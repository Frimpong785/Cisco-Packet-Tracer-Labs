# VLAN Configuration

## Objective

The objective of this lab is to configure Virtual Local Area Networks (VLANs) on a Cisco Layer 2 switch. VLANs are used to logically divide a physical network into separate broadcast domains, improving network security, performance, and management.

## Devices Used

- 2 Cisco 2960 Switch
- 12 PCs

## Network Topology

- PC0,PC1,PC8 and PC9 belong to VLAN 10 (HR)
- PC2,PC3,PC6 and PC7 belong to VLAN 20 (SALES)
- PC4,PC5,PC10 and PC11 belong to VLAN 20 (FINANCE)

## Configuration Tasks

- Assign host devices IP Address
- Create VLAN 10, VLAN 20 and VLAN 30
- Assign names to each VLAN
- Configure access ports
- Assign switch ports to the correct VLAN
- Configure trunk port between switches
- Verify VLAN configuration
- Test communication between vlans
NOTE: Devices in the same vlan will communicate whiles devices in different vlans will not communicate by default.

## Verification Commands

```bash
show vlan brief
show running-config
show interfaces switchport
```

## Skills Practiced

- Creating VLANs
- Naming VLANs
- Configuring Access Ports
- Assigning Interfaces to VLANs
- Configuring Trunk Ports
- Verifying VLAN Configuration

## Files Included

- VLAN.pkt
- configuration.txt
- notes.md
- images/topology.png

## Author

Kwame Anokye