
# SSH Notes

## What is SSH?

Secure Shell (SSH) is a secure network protocol used to remotely manage routers, switches, and other network devices. Unlike Telnet, SSH encrypts all communication, including usernames, passwords, and command output, protecting them from interception.

SSH uses TCP port 22.

## Why Use SSH?

- Encrypts all network traffic.
- Protects usernames and passwords.
- Prevents packet sniffing attacks.
- Provides secure remote administration.
- Recommended by Cisco for production networks.

## SSH Requirements

Before SSH can be enabled, you must:

- Configure a hostname.
- Configure an IP domain name.
- Create a local username and password.
- Generate RSA encryption keys.
- Enable SSH Version 2.
- Configure the VTY lines to use local login and accept only SSH connections.

## Important Commands

Configure hostname

```bash
hostname R1
```

Configure domain name

```bash
ip domain-name Frimp.local
```

Create a local user

```bash
username Admin secret Cisco
```

Generate RSA keys

```bash
crypto key generate rsa
```

Enable SSH Version 2

```bash
ip ssh version 2
```

Configure VTY lines

```bash
line vty 0 4
login local
transport input ssh
```

Verify SSH

```bash
show ip ssh
show ssh
show users
```

## Key Points

- SSH uses TCP port 22.
- SSH encrypts all communication.
- SSH is more secure than Telnet.
- RSA keys are required before SSH can operate.
- Local user authentication is commonly used with SSH.