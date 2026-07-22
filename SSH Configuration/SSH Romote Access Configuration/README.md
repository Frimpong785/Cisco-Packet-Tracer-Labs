# SSH Remote Access Configuration

## Objective

The objective of this lab is to configure Secure Shell (SSH) on a Cisco router and switch to allow secure remote management over an IP network.

## Devices Used

- 1 Cisco Router and a Switch
- 3 PCs

## Configuration Tasks

- Configure a hostname
- Configure a domain name
- Create a local user account
- Generate RSA encryption keys
- Enable SSH Version 2
- Configure VTY lines for SSH only
- Verify remote SSH access

## Verification Commands

```bash
show running-config
show ip interface brief
show ip ssh
show users
show ssh
```

From the PC:

```text
ssh -l admin IP Add
```

## Skills Practiced

- Secure Remote Access
- RSA Key Generation
- Local User Authentication
- SSH Version 2 Configuration
- VTY Line Security

## Files Included

- SSH-Remote-Access.pkt
- configuration.txt
- notes.md
- readme.md
- images/topology.png

## Author

Kwame Anokye
