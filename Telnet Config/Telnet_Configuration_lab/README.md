# Telnet Remote Access Configuration

## Objective

The objective of this lab is to configure Telnet remote access on a Cisco router or switch, allowing administrators to manage the device remotely over an IP network.

## Devices Used

- 1 Cisco Router and a Switch
- 3 PC

## Configuration Tasks

- Assign IP address to the router and host devices
- Configure a management IP address
- Configure the default gateway (for switches)
- Configure VTY lines
- Configure a Telnet password
- Enable Telnet login
- Verify remote connectivity

## Verification Commands

```bash
show running-config
show ip interface brief
show users
```

From the PC:

```text
telnet 192.168.1.1
```

## Skills Practiced

- Remote Device Management
- VTY Line Configuration
- Telnet Configuration
- IP Address Configuration
- Connectivity Testing

## Files Included

- Telnet-Remote-Access.pkt
- configuration.txt
- notes.md
- readme.md
- images/topology.png

## Author

Kwame Anokye