# Inter-VLAN Routing Notes

## What is Inter-VLAN Routing?

Inter-VLAN Routing is the process of allowing devices in different VLANs to communicate with one another. Since each VLAN is a separate broadcast domain, devices in different VLANs cannot communicate directly without a Layer 3 device.

The Layer 3 device can be:

- A router (Router-on-a-Stick)
- A multilayer (Layer 3) switch

## What is Router-on-a-Stick?

Router-on-a-Stick (ROAS) is a method of Inter-VLAN Routing where a single physical router interface is divided into multiple logical subinterfaces. Each subinterface is assigned to a VLAN and acts as the default gateway for that VLAN.

Communication between the router and the switch takes place over a single trunk link using IEEE 802.1Q tagging.

## How It Works

1. A PC sends traffic to its default gateway.
2. The switch tags the frame with the VLAN ID.
3. The frame travels across the trunk link.
4. The router receives the tagged frame on the appropriate subinterface.
5. The router routes the packet to the destination VLAN.
6. The packet is sent back to the switch and delivered to the destination device.

## Important Commands

Configure Trunk

```bash
interface fa0/24
switchport mode trunk
```

Configure Subinterface

```bash
interface g0/0.10
encapsulation dot1Q 10
ip address 192.168.10.1 255.255.255.0
```

Configure Native VLAN

```bash
interface g0/0.99
encapsulation dot1Q 99 native
ip address 192.168.99.1 255.255.255.0
```

Verify

```bash
show ip interface brief
show interfaces trunk
show vlan brief
show ip route
```

## Key Points

- Devices in different VLANs require a Layer 3 device to communicate.
- Router-on-a-Stick uses one physical interface with multiple subinterfaces.
- Each subinterface belongs to one VLAN.
- IEEE 802.1Q encapsulation identifies the VLAN for each subinterface.
- The switch port connected to the router must be configured as a trunk.