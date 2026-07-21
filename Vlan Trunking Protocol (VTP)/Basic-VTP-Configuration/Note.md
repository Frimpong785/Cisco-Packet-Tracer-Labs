# VTP Notes

## What is VTP?

VLAN Trunking Protocol (VTP) is a Cisco proprietary Layer 2 protocol that automatically distributes VLAN information between switches connected through trunk links. Instead of creating the same VLANs on every switch, you can create them once on a VTP Server and they are advertised to VTP Clients in the same VTP domain.

## Why Use VTP?

- Simplifies VLAN administration.
- Reduces configuration errors.
- Saves time when managing multiple switches.
- Keeps VLAN information synchronized.

## VTP Requirements

For VTP to work correctly:

- Switches must be in the same VTP domain.
- Trunk links must exist between switches.
- The VTP version must match.
- If configured, the VTP password must match.
- The switches must be able to exchange VTP advertisements.

## VTP Modes

### Server Mode

- Default mode on Cisco switches.
- Can create, modify and delete VLANs.
- Advertises VLAN information to other switches.
- Saves VLAN information in the VLAN database.

### Client Mode

- Cannot create or delete VLANs.
- Learns VLANs from the VTP Server.
- Forwards VTP advertisements.

### Transparent Mode

- Does not learn VLANs from the VTP Server.
- Does not advertise locally created VLANs through VTP.
- Forwards VTP advertisements received from other switches.
- VLANs created on a transparent switch are local to that switch.

## Important Commands

Configure VTP Domain

```bash
vtp domain CCNA
```

Configure VTP Mode

```bash
vtp mode server
```

Configure Password

```bash
vtp password cisco
```

Configure Version

```bash
vtp version 2
```

Verify

```bash
show vtp status
```

## Key Points

- VTP works only across trunk links.
- VLANs created on the Server are automatically learned by Clients.
- Transparent mode forwards VTP advertisements but maintains its own VLAN database.
- VTP does not replace the need for trunking—it depends on trunk links.Cisco switches, they   are stored in the VLAN database(vlan.dat).