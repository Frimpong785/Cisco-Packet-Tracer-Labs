# Inter-VLAN Routing Using a Layer 3 Switch

## What is a Layer 3 Switch?

A Layer 3 switch is a network device that combines the switching functions of a Layer 2 switch with the routing capabilities of a router. It can forward traffic within VLANs and route traffic between different VLANs.

## What is an SVI?

A Switch Virtual Interface (SVI) is a virtual Layer 3 interface associated with a VLAN. Each VLAN that requires routing is assigned an SVI with an IP address. This IP address becomes the default gateway for devices in that VLAN.

## Why Use a Layer 3 Switch?

- Faster routing because switching and routing occur in hardware.
- Eliminates the need for a separate router for Inter-VLAN Routing.
- Supports high-performance enterprise networks.
- Simplifies network design.

## How It Works

1. A PC sends traffic to its default gateway.
2. The default gateway is the SVI on the Layer 3 switch.
3. The Layer 3 switch receives the packet.
4. IP routing determines the destination VLAN.
5. The packet is forwarded to the destination VLAN through the appropriate access port or trunk.

## Important Commands

Enable IP Routing

```bash
ip routing
```

Create an SVI

```bash
interface vlan 10
 ip address 192.168.10.1 255.255.255.0
 no shutdown
```

Configure a Trunk

```bash
interface gigabitEthernet0/1
 switchport mode trunk
```

Verify

```bash
show ip interface brief
show ip route
show vlan brief
show interfaces trunk
```

## Key Points

- SVIs act as the default gateways for VLANs.
- IP routing must be enabled on the Layer 3 switch.
- Trunk links carry multiple VLANs between switches.
- Layer 3 switches provide faster Inter-VLAN Routing than Router-on-a-Stick.
- Each VLAN should have its own SVI with a unique IP address.