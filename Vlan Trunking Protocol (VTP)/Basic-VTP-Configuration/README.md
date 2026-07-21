# VTP (VLAN Trunking Protocol)

## Objective

The objective of this lab is to configure VLAN Trunking Protocol (VTP) on Cisco switches. VTP simplifies VLAN management by allowing VLAN information to be shared automatically between switches within the same VTP domain.

## Devices Used

- 5 Cisco 2960 Switches
- 2 PCs

## Configuration Tasks

- Configure VTP Domain
- Configure VTP Password
- Configure VTP Version
- Configure VTP Modes (Server, Client and Transparent)
- Configure Trunk Links
- Create VLANs on the VTP Server
- Verify VLAN propagation

## Verification Commands

```bash
show vtp status
show vlan brief
show interfaces trunk
show running-config
```

## Skills Practiced

- VTP Server Configuration
- VTP Client Configuration
- VTP Transparent Mode
- Trunk Configuration
- VLAN Propagation
- Troubleshooting VTP

## Files Included

- VTP.pkt
- configuration.txt
- notes.md
- readme.md
- images/topology.png

## Author

Kwame Anokye