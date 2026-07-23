# EtherChannel Notes

## What is EtherChannel?

EtherChannel is a Cisco technology that combines two or more physical Ethernet links into one logical interface called a Port-Channel. To the switch, the bundled links appear as a single connection.

EtherChannel increases available bandwidth while also providing redundancy. If one physical link fails, the remaining links continue forwarding traffic without interrupting communication.

## Benefits of EtherChannel

- Increases bandwidth by combining multiple links.
- Provides redundancy and fault tolerance.
- Prevents blocked links while working with Spanning Tree Protocol (STP).
- Simplifies switch configuration because the Port-Channel is managed as a single interface.
- Improves load balancing across multiple links.

## EtherChannel Protocols

### PAgP (Port Aggregation Protocol)

- Cisco proprietary protocol.
- Modes:
  - desirable
  - auto

### LACP (Link Aggregation Control Protocol)

- IEEE 802.3ad / IEEE 802.1AX standard.
- Works between Cisco and non-Cisco devices.
- Modes:
  - active
  - passive

LACP is generally preferred because it is an open standard.

## EtherChannel Requirements

For EtherChannel to form successfully:

- All interfaces must have the same speed.
- All interfaces must have the same duplex setting.
- All interfaces must belong to the same VLAN (access mode) or have identical trunk settings (trunk mode).
- All interfaces must use the same EtherChannel protocol and compatible modes.

## Example Configuration (LACP)

```bash
interface range fa0/1 - 2
 channel-group 1 mode active
 exit

interface port-channel 1
 switchport mode trunk
```

## Verification Commands

```bash
show etherchannel summary
show interfaces port-channel 1
show interfaces trunk
```

## Key Points

- EtherChannel creates one logical interface from multiple physical interfaces.
- STP treats the Port-Channel as a single link.
- LACP uses **active** and **passive** modes.
- PAgP uses **desirable** and **auto** modes.
- All member interfaces must have matching configurations.