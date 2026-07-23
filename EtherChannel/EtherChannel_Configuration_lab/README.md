# EtherChannel Configuration

## Objective

The objective of this lab is to configure EtherChannel between two Cisco layer 2 switches and  layer 3 switches. EtherChannel combines multiple physical interfaces into a single logical interface to increase bandwidth, provide redundancy, and simplify network management.

## Devices Used

- 2 Cisco 2960 Layer 2 Switches
- 2 Cisco 3560 layer 3 Switchs
- 2 PCs
- 1 server

## Configuration Tasks

- Configure IP Address to end hosts and SVI 
- Configure Layer 2 etherChannel between ASW1 and DSW1 using LACP, configure it as trunk.
- Configure Layer 2 etherChannel between ASW1 and DSW1 using PAgP, configure it as trunk.
- Configure Layer 3 etherChannel between DSW1 and DSW2 using Static EtherChannel.
- Configure route to allow the PCs to reach the Server.
- configure the switches to load-balance based on soure and destination ip add.

## Verification Commands

```bash
show etherchannel summary
show interfaces port-channel 1
show interfaces trunk
show running-config
show etherchannel load-balance
```

## Skills Practiced

- EtherChannel Configuration
- LACP Configuration
- PAgP Configuration
- Port-Channel Configuration
- Trunk Configuration
- Verification and Troubleshooting

## Files Included

- EtherChannel.pkt
- configuration.txt
- notes.md
- readme.md
- images/topology.png

## Author

Kwame Anokye