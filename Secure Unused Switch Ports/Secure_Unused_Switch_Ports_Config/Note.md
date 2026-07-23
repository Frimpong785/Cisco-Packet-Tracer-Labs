# Secure Unused Switch Ports Notes

## What are Secure Unused Ports?

Unused switch ports should never be left active. An attacker could plug a device into an unused port and gain access to the network. To reduce this risk, network administrators secure unused ports by assigning them to an unused VLAN and placing them in the shutdown state.

## Why Secure Unused Ports?

- Prevents unauthorized physical access to the network.
- Reduces the risk of network attacks.
- Prevents accidental connections.
- Follows Cisco security best practices.

## Best Practices

- Configure unused ports as access ports.
- Assign unused ports to an unused VLAN (for example, VLAN 999).
- Shut down the unused ports.
- Clearly document which ports are intentionally disabled.

## Example Configuration

```bash
vlan 999
 name UNUSED

interface range fa0/10 - 24
 switchport mode access
 switchport access vlan 999
 shutdown
```

## Verification Commands

```bash
show interfaces status
show vlan brief
show running-config
```

## Key Points

- The `shutdown` command administratively disables the interface.
- The `no shutdown` command re-enables the interface.
- Assigning unused ports to an unused VLAN provides an additional layer of protection.
- This is a preventive security measure and is commonly implemented in enterprise networks.