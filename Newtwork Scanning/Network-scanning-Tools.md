# Network Scanning Tools

## Why Network Scanning Matters

Network scanning is used to identify devices, services, operating systems, and potential security weaknesses within a network.

Security professionals use scanning tools to:

- Discover active hosts
- Identify open ports
- Detect running services
- Enumerate network infrastructure
- Assess attack surfaces
- Verify security configurations

---

# Nmap

## Purpose

Network discovery and security auditing.

## Capabilities

- Host Discovery
- Port Scanning
- Service Enumeration
- Operating System Detection
- Version Detection
- Network Mapping

## Example

```bash
nmap 192.168.1.1
```

### Service Detection

```bash
nmap -sV 192.168.1.1
```

### Operating System Detection

```bash
nmap -O 192.168.1.1
```

### Aggressive Scan

```bash
nmap -A 192.168.1.1
```

### Common Uses

- Asset Discovery
- Attack Surface Identification
- Network Auditing
- Security Assessments

---

# Masscan

## Purpose

High-speed Internet-scale port scanning.

## Capabilities

- Extremely fast scanning
- Large network discovery
- Open port identification

## Example

```bash
masscan 192.168.1.0/24 -p80,443
```

### Common Uses

- Large Network Audits
- Internet-wide Research
- Exposure Identification

---

# Netdiscover

## Purpose

ARP-based network discovery.

## Capabilities

- Host Discovery
- MAC Address Enumeration
- Local Network Mapping

## Example

```bash
netdiscover
```

### Common Uses

- Internal Network Reconnaissance
- Device Discovery
- Network Inventory

---

# Angry IP Scanner

## Purpose

Graphical IP scanner for network discovery.

## Capabilities

- Host Discovery
- Port Scanning
- Service Detection

### Common Uses

- Network Auditing
- Device Enumeration
- Quick Assessments

---

# RustScan

## Purpose

Fast port scanning combined with Nmap integration.

## Capabilities

- Rapid Port Discovery
- Automated Nmap Enumeration
- Service Detection

## Example

```bash
rustscan -a 192.168.1.1
```

### Common Uses

- Penetration Testing
- Fast Enumeration
- Security Assessments

---

# Network Enumeration Workflow

## Step 1: Discover Hosts

Tools:

- Nmap
- Netdiscover
- Angry IP Scanner

Goal:

- Identify active devices

---

## Step 2: Identify Open Ports

Tools:

- Nmap
- RustScan
- Masscan

Goal:

- Discover exposed services

---

## Step 3: Enumerate Services

Tools:

- Nmap

Example:

```bash
nmap -sV target-ip
```

Goal:

- Determine software versions
- Identify potential vulnerabilities

---

## Step 4: Assess Security Risks

Analyze:

- Open ports
- Unnecessary services
- Outdated software
- Misconfigurations

---

# Practical Skills Demonstrated

- Host Discovery
- Port Scanning
- Service Enumeration
- Operating System Detection
- Attack Surface Analysis
- Network Mapping
- Security Auditing

---

# Career Applications

## SOC Analyst

Uses scanning tools to:

- Monitor network exposure
- Investigate suspicious systems
- Verify asset inventories

## Security Analyst

Uses scanning tools to:

- Assess attack surfaces
- Discover vulnerabilities
- Audit infrastructure

## Penetration Tester

Uses scanning tools to:

- Enumerate targets
- Discover services
- Identify attack vectors

---

# Key Takeaway

Network scanning tools provide visibility into network infrastructure and exposed services. They are essential for reconnaissance, vulnerability assessment, penetration testing, and security auditing.