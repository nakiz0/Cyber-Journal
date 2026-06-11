# Bash Scripting

## What is Bash Scripting?

Bash (Bourne Again Shell) is a command-line shell and scripting language commonly used in Linux and Unix-based operating systems.

Bash scripts automate repetitive tasks, manage systems, process files, and perform administrative operations efficiently.

In cybersecurity, Bash scripting is widely used for automation, reconnaissance, monitoring, and system administration.

---

## Why Bash Scripting Matters

Manually performing tasks such as:

- Checking system status
- Monitoring logs
- Managing users
- Scanning networks
- Updating software

can be time-consuming.

Bash scripting helps automate these tasks, improving efficiency and reducing human error.

---

# Basic Script Structure

## Example

```bash
#!/bin/bash

echo "Hello, World!"
```

### Components

#### Shebang

```bash
#!/bin/bash
```

Specifies the script interpreter.

#### Command

```bash
echo
```

Prints output to the terminal.

---

# Variables

## Example

```bash
#!/bin/bash

name="Amrit"

echo "Hello $name"
```

### Uses

- Store data
- User input
- System information

---

# User Input

## Example

```bash
#!/bin/bash

read -p "Enter your name: " name

echo "Welcome $name"
```

### Uses

- Interactive scripts
- Automation tools
- Administrative tasks

---

# Conditional Statements

## Example

```bash
#!/bin/bash

if [ $USER = "root" ]
then
    echo "Administrator Access"
else
    echo "Standard User"
fi
```

### Uses

- Access verification
- Security checks
- Decision making

---

# Loops

## For Loop

```bash
for i in {1..5}
do
    echo $i
done
```

### Uses

- Repetitive tasks
- Bulk operations
- Automation

---

## While Loop

```bash
count=1

while [ $count -le 5 ]
do
    echo $count
    count=$((count+1))
done
```

---

# Functions

## Example

```bash
greet() {
    echo "Welcome to Linux"
}

greet
```

### Benefits

- Reusable code
- Better organization
- Easier maintenance

---

# File Operations

## Create a File

```bash
touch file.txt
```

## Copy a File

```bash
cp file1.txt file2.txt
```

## Move a File

```bash
mv file1.txt backup/
```

## Delete a File

```bash
rm file.txt
```

---

# Process Management

## View Running Processes

```bash
ps aux
```

## Monitor Processes

```bash
top
```

## Terminate a Process

```bash
kill PID
```

### Cybersecurity Applications

- Process monitoring
- Malware detection
- Resource analysis

---

# Log Analysis

## Example

```bash
grep "Failed password" /var/log/auth.log
```

### Uses

- Detect failed logins
- Identify brute-force attacks
- Investigate incidents

---

# Network Commands

## Check IP Address

```bash
ip a
```

## Test Connectivity

```bash
ping google.com
```

## DNS Lookup

```bash
nslookup google.com
```

## View Open Ports

```bash
ss -tuln
```

### Cybersecurity Uses

- Network troubleshooting
- Service discovery
- Security auditing

---

# Automation Examples

## System Information Script

```bash
#!/bin/bash

echo "Hostname: $(hostname)"
echo "Current User: $(whoami)"
echo "IP Address:"
ip a
```

### Purpose

Collect system information automatically.

---

## User Enumeration Script

```bash
#!/bin/bash

cut -d: -f1 /etc/passwd
```

### Purpose

List local system users.

---

## Port Monitoring Script

```bash
#!/bin/bash

ss -tuln
```

### Purpose

Display listening ports and active services.

---

# Bash Scripting in Cybersecurity

## Reconnaissance

Automate:

- DNS Lookups
- Host Discovery
- Service Enumeration

---

## Security Auditing

Automate:

- User Audits
- File Permission Checks
- Service Monitoring

---

## Incident Response

Automate:

- Log Analysis
- Evidence Collection
- System Information Gathering

---

## System Administration

Automate:

- Backups
- Updates
- User Management
- Service Management

---

# Common Commands

## File Management

```bash
ls
cd
pwd
cp
mv
rm
find
```

## Text Processing

```bash
cat
grep
awk
sed
sort
```

## Networking

```bash
ping
traceroute
nslookup
ss
netstat
```

## System Information

```bash
hostname
whoami
uname
df
free
```

---

# Practical Experience

### Linux Administration

- System Configuration
- Package Management
- Service Management

### Networking

- IP Configuration
- DNS Troubleshooting
- Port Monitoring

### Security

- Log Analysis
- User Enumeration
- Service Auditing

### Automation

- Administrative Tasks
- Security Checks
- Reporting

---

# Skills Demonstrated

- Linux Administration
- Bash Scripting
- Process Management
- Network Troubleshooting
- Security Automation
- Log Analysis
- System Monitoring
- Command-Line Proficiency

---

# Key Takeaway

Bash scripting is an essential skill for cybersecurity professionals because it enables automation, system administration, security auditing, log analysis, and incident response. Strong Bash skills improve efficiency and provide deeper control over Linux-based environments commonly used in cybersecurity.