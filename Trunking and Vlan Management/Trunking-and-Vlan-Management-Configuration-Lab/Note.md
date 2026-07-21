# Trunking and VLAN Management Notes

## What is a Trunk Port?

A trunk port is a switch port that carries traffic for multiple VLANs over a single physical link between network devices. Cisco switches use IEEE 802.1Q tagging to identify the VLAN to which each frame belongs.

---

## What is an Allowed VLAN?

By default, a trunk carries all VLANs.

The **allowed VLAN** feature limits which VLANs are permitted to cross the trunk. This improves security and reduces unnecessary traffic.

Example:

```bash
switchport trunk allowed vlan 10,20,30
```

Only VLANs 10, 20 and 30 are allowed across the trunk.

To remove a VLAN from the allowed list:

```bash
switchport trunk allowed vlan remove 20
```

To add it back:

```bash
switchport trunk allowed vlan add 20
```




## What is a Native VLAN?

The native VLAN is the VLAN used for untagged frames on an IEEE 802.1Q trunk.

By default, the native VLAN is VLAN 1.

It is recommended to change the native VLAN to another unused VLAN for better security.

Example:

```bash
vlan 99

interface fa0/24
switchport mode trunk
switchport trunk native vlan 99
```

Both ends of the trunk must use the same native VLAN. A mismatch can cause connectivity issues and generate Cisco warnings.## Security Features of the Native VLAN

## Security Features of the Native VLA
By default, Cisco switches use VLAN 1 as the native VLAN. For better security, network administrators should change the native VLAN to an unused VLAN, such as VLAN 99, and avoid assigning user devices to it.

Changing the native VLAN helps:

- Reduce the risk of VLAN hopping attacks that exploit the default native VLAN.
- Prevent unauthorized access through untagged frames.
- Separate management and user traffic from the default VLAN.
- Follow Cisco security best practices by avoiding the use of VLAN 1 for production traffic.

**Best Practice:** Configure the same native VLAN on both ends of the trunk link and ensure that no end-user devices are connected to the native VLAN.





## Important Commands

Configure Trunk

```bash
switchport mode trunk
```

Configure Allowed VLANs

```bash
switchport trunk allowed vlan 10,20,30
```

Remove a VLAN

```bash
switchport trunk allowed vlan remove 20
```

Configure Native VLAN

```bash
switchport trunk native vlan 99
```


Verify

```bash
show interfaces trunk
show interfaces switchport
```

## Key Points

- Trunks carry traffic for multiple VLANs.
- Allowed VLANs control which VLANs cross a trunk.
- Native VLAN carries untagged traffic.
- Native VLANs must match on both ends of a trunk.