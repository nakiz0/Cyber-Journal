# Networking Fundamentals for Cybersecurity

## Why Networking Matters

Every cyber attack, security assessment, vulnerability scan, and web application relies on networking.

A strong understanding of networking helps security professionals:

- Identify attack surfaces
- Analyze network traffic
- Troubleshoot connectivity issues
- Detect malicious activity
- Secure network infrastructure

---

# IP Addressing

## What is an IP Address?

An IP (Internet Protocol) Address is a unique identifier assigned to a device on a network.

Example:

```text
192.168.1.10
```

Think of it as the address of a device on a network.

### Types

#### Public IP

Used on the Internet.

Example:

```text
103.x.x.x
```

Assigned by an ISP.

#### Private IP

Used within local networks.

Examples:

```text
192.168.x.x
10.x.x.x
172.16.x.x - 172.31.x.x
```

---

# Subnet Mask

## Purpose

Determines which portion of an IP address belongs to:

- Network
- Host

Example:

```text
IP Address: 192.168.1.10
Subnet Mask: 255.255.255.0
CIDR: /24
```

### Why It Matters

Used for:

- Network segmentation
- Routing
- Device communication

---

# CIDR Notation

## Example

```text
192.168.1.0/24
```

The number after "/" represents the number of network bits.

### Common CIDR Ranges

| CIDR | Hosts |
|--------|--------|
| /24 | 254 |
| /25 | 126 |
| /26 | 62 |
| /27 | 30 |

---

# MAC Address

## What is a MAC Address?

A hardware address assigned to a network interface card.

Example:

```text
00:1A:2B:3C:4D:5E
```

### Purpose

Used for communication inside local networks.

---

# DNS (Domain Name System)

## Purpose

Translates domain names into IP addresses.

Example:

```text
google.com
↓
142.250.x.x
```

### Common DNS Records

#### A Record

Maps a domain to an IPv4 address.

#### AAAA Record

Maps a domain to an IPv6 address.

#### MX Record

Mail server information.

#### CNAME Record

Alias for another domain.

#### TXT Record

Additional domain information.

### Security Relevance

- DNS Enumeration
- DNS Spoofing
- DNS Tunneling
- DNS Monitoring

---

# DHCP (Dynamic Host Configuration Protocol)

## Purpose

Automatically assigns:

- IP Address
- Gateway
- DNS Server
- Subnet Mask

### DHCP Process

1. Discover
2. Offer
3. Request
4. Acknowledge

Known as:

```text
DORA
```

### Security Relevance

- Rogue DHCP Detection
- Network Auditing
- IP Management

---

# Gateway

## Purpose

Allows devices to communicate outside their local network.

Example:

```text
192.168.1.1
```

Usually the router.

---

# ARP (Address Resolution Protocol)

## Purpose

Maps:

```text
IP Address
↓
MAC Address
```

### Example

```text
192.168.1.10
↓
00:1A:2B:3C:4D:5E
```

### Security Relevance

- ARP Spoofing
- MITM Attacks
- Network Monitoring

---

# Ports

## Purpose

Allow multiple services to run on a single system.

### Common Ports

| Port | Service |
|--------|--------|
| 20/21 | FTP |
| 22 | SSH |
| 23 | Telnet |
| 25 | SMTP |
| 53 | DNS |
| 80 | HTTP |
| 110 | POP3 |
| 143 | IMAP |
| 443 | HTTPS |
| 3306 | MySQL |

---

# TCP

## Purpose

Reliable communication protocol.

### Features

- Connection Oriented
- Reliable Delivery
- Error Checking
- Flow Control

### TCP Handshake

```text
SYN
↓
SYN-ACK
↓
ACK
```

### Security Relevance

- Port Scanning
- Session Analysis
- Firewall Rules

---

# UDP

## Purpose

Fast communication without guaranteed delivery.

### Features

- Connectionless
- Faster
- No Handshake

### Common Services

- DNS
- VoIP
- Streaming

---

# HTTP

## Purpose

Transfers web content.

### Example

```text
http://example.com
```

### Common Methods

- GET
- POST
- PUT
- DELETE

---

# HTTPS

## Purpose

Secure version of HTTP.

### Features

- Encryption
- Authentication
- Integrity

Uses:

```text
TLS/SSL
```

### Security Importance

Protects:

- Passwords
- Sessions
- Sensitive Data

---

# Sockets

## What is a Socket?

A socket is the endpoint of communication between two devices.

Think of it as:

```text
IP Address + Port
```

Example:

```text
192.168.1.10:80
```

### Python Example

```python
import socket

s = socket.socket()

s.connect(("google.com",80))
```

### Security Relevance

- Port Scanners
- Network Tools
- Client-Server Applications

---

# Routing

## Purpose

Moves packets between networks.

### Routing Devices

- Routers
- Layer 3 Switches

### Security Importance

- Traffic Control
- Network Segmentation
- Access Management

---

# Network Troubleshooting

## Common Tools

### Ping

Tests connectivity.

```bash
ping google.com
```

### Traceroute

Shows packet path.

```bash
traceroute google.com
```

### nslookup

DNS troubleshooting.

```bash
nslookup google.com
```

### netstat

Network connections.

```bash
netstat -an
```

### ss

Linux socket statistics.

```bash
ss -tuln
```

---

# Key Takeaway

Networking forms the foundation of cybersecurity. Understanding IP addressing, DNS, DHCP, TCP/IP, sockets, ports, routing, and network troubleshooting is essential for penetration testing, security analysis, incident response, and cloud security.