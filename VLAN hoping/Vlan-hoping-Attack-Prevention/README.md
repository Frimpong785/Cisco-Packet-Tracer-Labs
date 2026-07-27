- 
# VLAN Hopping Attack Prevention

## Objective

The objective of this lab is to implement Layer 2 security measures to reduce the risk of VLAN hopping attacks by disabling Dynamic Trunking Protocol (DTP), manually configuring trunk ports, disabling CDP where appropriate, and securing unused ports.

## Devices Used

- 3 Cisco 2960 Switches
- 6 PCs

## Configuration Tasks

- Configure access ports
- Configure trunk ports manually
- Disable DTP negotiation
- Disable CDP on selected interfaces
- Verify trunk operation
- Verify CDP status

## Verification Commands

```bash
show interfaces trunk
show interfaces switchport
show cdp
show cdp neighbors
show running-config
```

## Skills Practiced

- VLAN Hopping Prevention
- DTP Security
- CDP Configuration
- Trunk Security
- Layer 2 Security Best Practices

## Files Included

- VLAN-Hopping-Prevention.pkt
- configuration.txt
- notes.md
- readme.md
- images/topology.png

## Author

Kwame Anokye Frimpong