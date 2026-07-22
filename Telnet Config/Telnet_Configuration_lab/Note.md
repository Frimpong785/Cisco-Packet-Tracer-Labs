# Telnet Notes

## What is Telnet?

Telnet is a network protocol used to remotely access and manage network devices through the Command-Line Interface (CLI). It operates over TCP port 23.

Instead of connecting a console cable directly to the device, an administrator can connect over the network using Telnet.

## How Telnet Works

1. The administrator assigns an IP address to the router or switch.
2. The VTY (Virtual Terminal) lines are configured with a password.
3. A remote PC connects using the Telnet command.
4. After successful authentication, the administrator can manage the device remotely.

## Advantages

- Enables remote administration.
- Eliminates the need for physical access.
- Simple to configure.

## Disadvantages

- Sends usernames and passwords in plain text.
- Traffic is not encrypted.
- Vulnerable to packet sniffing and password theft.

Because of these security risks, SSH is recommended instead of Telnet in production networks.

## Important Commands

Configure VTY lines

```bash
line vty 0 4
password cisco
login
transport input telnet
```

Configure a management IP (Switch)

```bash
interface vlan 1
ip address 192.168.2.254 255.255.255.0
no shutdown
```

Configure the default gateway

```bash
ip default-gateway 192.168.2.1
```

Verify

```bash
show users
show running-config
```

## Key Points

- Telnet uses TCP port 23.
- Telnet transmits data in plain text.
- Telnet requires an IP address on the device.
- VTY lines must be configured.
- SSH is more secure than Telnet because it encrypts traffic.