# VLAN Notes

## What is a VLAN?

A Virtual Local Area Network (VLAN) is a logical grouping of devices within the same physical switch. Instead of separating devices using different switches, VLANs allow a single switch to be divided into multiple independent networks.

Each VLAN forms its own broadcast domain. Devices within the same VLAN can communicate directly, while communication between different VLANs requires a Layer 3 device such as a router or multilayer switch.

## Why Use VLANs?

- Improves network security by separating departments.
- Reduces unnecessary broadcast traffic.
- Makes network management easier.
- Allows users to be grouped by function instead of physical location.
- Improves overall network performance.

## VLAN Types

- Default VLAN (VLAN 1)
- Data VLAN
- Management VLAN
- Native VLAN
- Voice VLAN

## Important Commands

Create a VLAN

```bash
vlan 10
name Sales
```

Assign a port to a VLAN

```bash
interface fa0/1
switchport mode access
switchport access vlan 10
```

Verify VLANs

```bash
show vlan brief
```

Delete a VLAN

```bash
no vlan 10
```

## Key Points

- VLANs create separate broadcast domains.
- Devices in different VLANs cannot communicate without inter-VLAN routing.
- Access ports belong to only one VLAN.
- VLAN information is stored in the vlan.dat file on Cisco switches.