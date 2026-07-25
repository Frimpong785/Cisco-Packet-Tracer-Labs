# Inter-VLAN Routing Using a Layer 3 Switch

## Objective

The objective of this lab is to configure Inter-VLAN Routing using a Cisco Layer 3 switch. Switch Virtual Interfaces (SVIs) are configured to route traffic between VLANs without using a separate router.

## Devices Used

- 1 Cisco Layer 3 Switch (3560)
- 1 Cisco Layer 2 Switch (2960)
- 4 PCs

## Network Topology

- VLAN 10 (Sales)
- VLAN 20 (HR)
- Layer 2 Switch connected to the Layer 3 Switch through a trunk link
- Four PCs connected to the Layer 2 Switch

## Configuration Tasks

- Create VLANs
- Configure access ports
- Configure a trunk link
- Create Switch Virtual Interfaces (SVIs)
- Assign IP addresses to the SVIs
- Enable IP routing
- Verify communication between VLANs

## Verification Commands

```bash
show vlan brief
show interfaces trunk
show ip interface brief
show ip route
show running-config
```

## Skills Practiced

- VLAN Configuration
- Trunk Configuration
- SVI Configuration
- IP Routing
- Inter-VLAN Routing
- Connectivity Verification

## Files Included

- Inter-VLAN-Routing-Layer3-Switch.pkt
- configuration.txt
- notes.md
- readme.md
- images/topology.png

## Author

Kwame Anokye Frimpong