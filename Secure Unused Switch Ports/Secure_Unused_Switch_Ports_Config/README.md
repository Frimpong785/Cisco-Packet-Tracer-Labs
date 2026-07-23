# Secure Unused Switch Ports

## Objective

The objective of this lab is to secure unused switch ports by assigning them to an unused VLAN and placing them in the shutdown state. This prevents unauthorized users from connecting devices to inactive switch ports.

## Devices Used

- 2 Cisco 2960 Switch
- 10 PCs

## Configuration Tasks

- Create valid VLANs and name them.
- Create a blackhole/fake VLAN and name it.
- Identify all usable ports and assign them respective valid VLANs.
- Identify all unuse ports,assign them the blackhole vlan and shutdown all of them.
- Create etherchannel.
- identify and configure trunk links then deny the blackhole vlan through it.
- try to connect Hacker PCs to any unuse port. 

## Verification Commands

```bash
show interfaces status
show running-config
show vlan brief
```

## Skills Practiced

- Switch Port Security Best Practices
- Interface Administration
- VLAN Assignment
- Interface Shutdown
- Configuration Verification

## Files Included

- Secure-Unused-Ports.pkt
- configuration.txt
- notes.md
- readme.md
- images/topology.png

## Author

Kwame Anokye Frimpong