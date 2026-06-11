# Cloud Security and AWS

## What is Cloud Security?

Cloud Security is the practice of protecting cloud-based systems, applications, networks, and data from cyber threats.

It involves implementing security controls, monitoring cloud resources, managing identities, and ensuring the confidentiality, integrity, and availability of cloud environments.

---

## Why Cloud Security Matters

Organizations increasingly rely on cloud services to host applications and store sensitive information.

Without proper security controls, cloud environments can become targets for:

- Data Breaches
- Misconfigurations
- Unauthorized Access
- Account Compromise
- Malware Infections
- Insider Threats

Cloud Security helps reduce these risks and maintain a secure infrastructure.

---

# What is AWS?

Amazon Web Services (AWS) is one of the world's leading cloud computing platforms.

AWS provides on-demand services for:

- Computing
- Storage
- Networking
- Security
- Databases
- Artificial Intelligence
- Monitoring

---

# AWS Shared Responsibility Model

## Understanding Responsibility

AWS follows a Shared Responsibility Model.

### AWS is Responsible For

- Physical Security
- Data Centers
- Hardware
- Networking Infrastructure
- Hypervisors

### Customers are Responsible For

- User Management
- Access Control
- Data Protection
- Security Configurations
- Operating System Security
- Application Security

### Key Principle

```text
AWS secures the Cloud
Customers secure what is in the Cloud
```

---

# Identity and Access Management (IAM)

## Purpose

IAM controls who can access AWS resources and what actions they can perform.

### Features

- User Management
- Group Management
- Role-Based Access
- Permission Policies

### Security Best Practices

- Follow Least Privilege
- Avoid Root Account Usage
- Use Roles Instead of Long-Term Credentials
- Regularly Review Permissions

---

# Multi-Factor Authentication (MFA)

## Purpose

Adds an additional layer of security beyond passwords.

### Benefits

- Protects AWS Accounts
- Reduces Account Takeover Risks
- Improves Identity Security

### Recommended For

- Root Accounts
- Administrative Accounts
- Sensitive Environments

---

# Amazon EC2

## Purpose

Provides virtual servers in the cloud.

### Practical Experience

- Launching EC2 Instances
- Connecting via SSH
- Managing Security Groups
- Basic Server Administration

### Security Considerations

- Restrict Open Ports
- Disable Unnecessary Services
- Apply Security Updates
- Use Strong Authentication

---

# Security Groups

## Purpose

Act as virtual firewalls for AWS resources.

### Controls

- Inbound Traffic
- Outbound Traffic

### Example

Allow:

```text
SSH (22)
HTTPS (443)
```

Block:

```text
Unnecessary Services
Unused Ports
```

### Security Benefits

- Network Segmentation
- Reduced Attack Surface

---

# Amazon S3

## Purpose

Object storage service used for storing files and data.

### Practical Experience

- Creating Buckets
- Uploading Files
- Managing Permissions

### Security Risks

- Publicly Accessible Buckets
- Misconfigured Permissions
- Data Exposure

### Security Best Practices

- Enable Encryption
- Restrict Public Access
- Apply Least Privilege

---

# Virtual Private Cloud (VPC)

## Purpose

Provides isolated cloud networking environments.

### Features

- Private Networks
- Subnets
- Route Tables
- Security Controls

### Security Benefits

- Network Isolation
- Controlled Traffic Flow
- Improved Infrastructure Security

---

# AWS Monitoring and Logging

## CloudWatch

Used for:

- Monitoring Resources
- Performance Analysis
- Alerting

### Benefits

- Early Threat Detection
- Resource Monitoring
- Incident Investigation

---

## CloudTrail

Used for:

- Logging AWS Activities
- Tracking API Calls
- Auditing User Actions

### Security Benefits

- Accountability
- Incident Response
- Compliance Monitoring

---

# Encryption in AWS

## Data at Rest

Protect stored data using:

- S3 Encryption
- EBS Encryption

### Benefits

- Protects Sensitive Information
- Reduces Data Exposure Risks

---

## Data in Transit

Protect communication using:

- HTTPS
- TLS

### Benefits

- Prevents Data Interception
- Secures Network Communication

---

# Common Cloud Security Risks

## Misconfigurations

Examples:

- Public S3 Buckets
- Excessive Permissions
- Open Security Groups

---

## Weak Identity Management

Examples:

- Shared Accounts
- Weak Passwords
- Missing MFA

---

## Unpatched Systems

Examples:

- Vulnerable EC2 Instances
- Outdated Software

---

## Data Exposure

Examples:

- Public Databases
- Unencrypted Storage

---

# Cloud Security Best Practices

## Identity Security

- Enable MFA
- Use IAM Roles
- Apply Least Privilege

## Network Security

- Configure Security Groups
- Use Private Subnets
- Restrict Public Access

## Monitoring

- Enable CloudTrail
- Configure CloudWatch Alerts
- Review Logs Regularly

## Data Protection

- Encrypt Sensitive Data
- Secure Backups
- Restrict Storage Permissions

---

# Practical Experience

## AWS Services Used

### EC2

- Virtual Machine Deployment
- Linux Server Management
- SSH Access Configuration

### S3

- Object Storage Management
- Bucket Configuration
- Access Control

### IAM

- User Management
- Permission Configuration
- Security Policy Management

### Security Groups

- Firewall Rule Configuration
- Network Access Management

### VPC

- Cloud Network Fundamentals
- Subnet Configuration

---

# Skills Demonstrated

- Cloud Computing Fundamentals
- AWS Infrastructure Management
- Identity and Access Management (IAM)
- EC2 Deployment and Administration
- S3 Storage Management
- Security Group Configuration
- Cloud Monitoring and Logging
- Cloud Security Best Practices

---

# Career Applications

## Cloud Security Engineer

Uses AWS to:

- Secure Cloud Infrastructure
- Monitor Cloud Resources
- Implement Security Controls

## Security Analyst

Uses AWS to:

- Investigate Cloud Incidents
- Review Security Logs
- Assess Cloud Risks

## DevSecOps Engineer

Uses AWS to:

- Automate Security Controls
- Secure CI/CD Pipelines
- Monitor Cloud Environments

---

# Key Takeaway

Cloud Security focuses on protecting cloud infrastructure, applications, and data from cyber threats. Understanding AWS services such as EC2, S3, IAM, VPC, CloudWatch, and CloudTrail provides a strong foundation for securing modern cloud environments and preparing for cloud-focused cybersecurity roles.