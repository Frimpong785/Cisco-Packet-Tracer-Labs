# Inter-VLAN Routing (Router-on-a-Stick)

## Objective

The objective of this lab is to configure Inter-VLAN Routing using the Router-on-a-Stick method. This allows devices in different VLANs to communicate through a router using IEEE 802.1Q subinterfaces.

## Devices Used

- 1 Cisco Router
- 1 Cisco 2960 Switch
- 7 PCs

## Network Topology

- VLAN 10 (Sales)
- VLAN 20 (HR)
- One trunk link between the router and the switch

## Configuration Tasks

- Create VLANs
- Assign access ports to VLANs
- Configure a trunk port
- Configure router subinterfaces
- Enable 802.1Q encapsulation
- Assign gateway IP addresses
- Verify communication between VLANs

## Verification Commands

```bash
show vlan brief
show interfaces trunk
show ip interface brief
show running-config
show ip route
```

## Skills Practiced

- VLAN Configuration
- Trunk Configuration
- Router Subinterfaces
- 802.1Q Encapsulation
- Inter-VLAN Routing
- Connectivity Verification

## Files Included

- Inter-VLAN-Routing.pkt
- configuration.txt
- notes.md
- readme.md
- images/topology.png

## Author

Kwame Anokye Frimpong