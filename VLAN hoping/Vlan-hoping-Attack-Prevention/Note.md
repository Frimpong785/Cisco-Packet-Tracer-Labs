# VLAN Hopping Prevention Notes

## What is a VLAN Hopping Attack?

A VLAN hopping attack is a Layer 2 attack in which an attacker attempts to send traffic into a VLAN they are not authorized to access. This can allow unauthorized communication with devices in other VLANs.

Two common techniques are:

1. **Switch Spoofing** – The attacker pretends to be a switch and attempts to negotiate a trunk link using Dynamic Trunking Protocol (DTP).

2. **Double-Tagging** – The attacker sends frames with two VLAN tags to try to reach another VLAN. This attack mainly targets the native VLAN.

## Preventing VLAN Hopping

### 1. Disable DTP Negotiation

Configure trunk ports manually and disable DTP.

```bash
interface fa0/24
 switchport mode trunk
 switchport nonegotiate
```

The `switchport nonegotiate` command stops the switch from sending DTP packets, preventing trunk negotiation on that interface.

### 2. Disable CDP on Untrusted Interfaces

Cisco Discovery Protocol (CDP) shares information such as device names, software versions and interface details. An attacker could use this information to learn about the network.

Disable CDP on interfaces connected to end devices:

```bash
interface fa0/1
 no cdp enable
```

To disable CDP globally:

```bash
no cdp run
```

### 3. Secure Access Ports

Configure user-facing ports as access ports so they cannot negotiate a trunk.

```bash
switchport mode access
```

### 4. Change the Native VLAN

Do not use VLAN 1 as the native VLAN. Configure an unused VLAN instead.

```bash
switchport trunk native vlan 99
```

### Important Commands

Disable DTP

```bash
switchport nonegotiate
```

Disable CDP on an Interface

```bash
no cdp enable
```

Disable CDP Globally

```bash
no cdp run
```

Verify

```bash
show interfaces switchport
show interfaces trunk
show cdp
show cdp neighbors
```

## Key Points

- Disable DTP on manually configured trunk ports.
- Configure end-user ports as access ports.
- Disable CDP on untrusted or user-facing interfaces when it is not needed.
- Avoid using VLAN 1 as the native VLAN.
- Shut down unused ports and place them in an unused VLAN.