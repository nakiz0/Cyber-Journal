# Cryptography

## What is Cryptography?

Cryptography is the science of protecting information by converting readable data (plaintext) into an unreadable format (ciphertext).

Its primary objectives are:

- Confidentiality
- Integrity
- Authentication
- Non-Repudiation

---

# Why Cryptography Matters

Cryptography protects:

- Passwords
- Banking Transactions
- Cloud Data
- Emails
- VPN Traffic
- Web Applications
- Wireless Networks

Without cryptography, sensitive information could be intercepted and read by attackers.

---

# Core Security Principles

## Confidentiality

Ensures only authorized users can access data.

### Example

```text
Plaintext → Encryption → Ciphertext
```

---

## Integrity

Ensures data has not been modified.

### Common Methods

- Hashing
- Digital Signatures

---

## Authentication

Verifies identity.

### Examples

- Passwords
- Certificates
- Digital Signatures

---

## Non-Repudiation

Prevents users from denying their actions.

### Example

Digital signatures prove who signed a document.

---

# Symmetric Encryption

## What is Symmetric Encryption?

Symmetric encryption uses a single key for both encryption and decryption.

### Flow

```text
Plaintext
    ↓
Encryption
    ↓
Secret Key
    ↓
Ciphertext
    ↓
Secret Key
    ↓
Decryption
    ↓
Plaintext
```

---

## Advantages

- Fast
- Efficient
- Low Resource Usage
- Ideal for Large Data

---

## Disadvantages

- Key Sharing Problem
- Difficult Key Management

---

# AES (Advanced Encryption Standard)

## Overview

AES is the current industry standard encryption algorithm.

### Key Sizes

- AES-128
- AES-192
- AES-256

### Uses

- HTTPS
- VPNs
- Disk Encryption
- Cloud Storage
- Wi-Fi Security (WPA2/WPA3)

### Advantages

- Extremely Secure
- Fast Performance
- Industry Standard

### Disadvantages

- Requires Secure Key Exchange

---

# DES (Data Encryption Standard)

## Overview

Older encryption standard.

### Key Size

```text
56-bit
```

### Uses

- Legacy Systems

### Advantages

- Historically Important

### Disadvantages

- Easily Brute Forced
- Obsolete

---

# Triple DES (3DES)

## Overview

Improved version of DES.

### How it Works

```text
Encrypt
↓
Decrypt
↓
Encrypt
```

### Uses

- Legacy Banking Systems

### Advantages

- Stronger than DES

### Disadvantages

- Slow
- Being Phased Out

---

# Blowfish

## Overview

Symmetric block cipher developed by Bruce Schneier.

### Key Size

```text
32-bit to 448-bit
```

### Uses

- Password Managers
- Legacy Software

### Advantages

- Fast
- Free
- Strong Security

### Disadvantages

- Small Block Size
- Older Design

---

# Twofish

## Overview

Successor to Blowfish.

### Uses

- File Encryption
- Secure Storage

### Advantages

- Highly Secure
- Flexible Key Sizes

### Disadvantages

- Less Popular Than AES

---

# ChaCha20

## Overview

Modern stream cipher developed by Daniel Bernstein.

### Uses

- VPNs
- Mobile Devices
- TLS

### Advantages

- Fast on Mobile Devices
- Strong Security
- Efficient

### Disadvantages

- Less Common Than AES

---

# Asymmetric Encryption

## What is Asymmetric Encryption?

Asymmetric encryption uses two keys.

### Public Key

Used for Encryption.

### Private Key

Used for Decryption.

---

## Flow

```text
Sender
   ↓
Public Key
   ↓
Encryption
   ↓
Ciphertext
   ↓
Private Key
   ↓
Decryption
   ↓
Receiver
```

---

## Advantages

- Secure Key Exchange
- Supports Digital Signatures

---

## Disadvantages

- Slower Than Symmetric Encryption
- Higher Computational Cost

---

# RSA (Rivest-Shamir-Adleman)

## Overview

Most widely used public-key algorithm.

### Key Sizes

- 2048-bit
- 3072-bit
- 4096-bit

### Uses

- HTTPS
- SSL/TLS
- Digital Signatures
- Secure Email

### Advantages

- Highly Trusted
- Widely Supported

### Disadvantages

- Slower Than AES
- Computationally Expensive

---

## RSA Encryption Flow

```text
Receiver Creates:

Public Key
Private Key

        ↓

Public Key Shared

        ↓

Sender Encrypts Data

        ↓

Ciphertext Sent

        ↓

Receiver Uses Private Key

        ↓

Original Data Restored
```

---

# ECC (Elliptic Curve Cryptography)

## Overview

Modern public-key cryptography using elliptic curves.

### Uses

- Cryptocurrency
- Mobile Security
- SSL/TLS
- Digital Signatures

### Advantages

- Smaller Keys
- Faster Operations
- Strong Security

### Disadvantages

- More Complex Mathematics

---

# Diffie-Hellman

## Purpose

Securely exchange encryption keys.

### Uses

- VPNs
- TLS Handshakes

### Advantages

- Secure Key Exchange

### Disadvantages

- Does Not Encrypt Data Directly

---

# Hashing

## What is Hashing?

Hashing converts data into a fixed-length output called a hash.

### Important

Hashes cannot be reversed.

---

## Hashing Flow

```text
Password
    ↓
Hash Function
    ↓
Hash Value
```

---

# MD5

## Overview

One of the oldest hashing algorithms.

### Output

```text
128-bit Hash
```

### Uses

- File Integrity Checks

### Advantages

- Fast

### Disadvantages

- Broken
- Collision Vulnerabilities

### Status

Not Recommended

---

# SHA-1

## Overview

Successor to MD5.

### Output

```text
160-bit Hash
```

### Advantages

- Better Than MD5

### Disadvantages

- Collision Attacks

### Status

Deprecated

---

# SHA-256

## Overview

Part of the SHA-2 family.

### Output

```text
256-bit Hash
```

### Uses

- Blockchain
- Certificates
- Password Storage
- Integrity Verification

### Advantages

- Strong Security
- Industry Standard

---

# SHA-512

## Overview

Stronger version of SHA-256.

### Output

```text
512-bit Hash
```

### Uses

- Government Systems
- Enterprise Security

---

# Password Hashing Algorithms

## bcrypt

### Uses

- Password Storage

### Advantages

- Salted
- Slow Against Attackers

---

## Argon2

### Uses

- Modern Password Storage

### Advantages

- Winner of Password Hashing Competition
- Highly Secure

### Status

Recommended

---

## PBKDF2

### Uses

- Enterprise Password Storage

### Advantages

- Widely Supported

---

# Digital Signatures

## Purpose

Verify:

- Identity
- Integrity
- Authenticity

---

## Digital Signature Flow

```text
Document
    ↓
Hash Created
    ↓
Private Key Signs Hash
    ↓
Signature Generated

Receiver:

Document
+
Signature

    ↓

Public Key Verification

    ↓

Valid or Invalid
```

---

# SSL/TLS Encryption Flow

## How HTTPS Actually Works

### Step 1

Browser connects to website.

### Step 2

Website sends certificate.

### Step 3

Browser verifies certificate.

### Step 4

RSA/ECC exchanges a session key.

### Step 5

AES or ChaCha20 encrypts communication.

### Step 6

Secure HTTPS session established.

---

# Symmetric vs Asymmetric Encryption

| Feature | Symmetric | Asymmetric |
|----------|------------|------------|
| Keys | One | Two |
| Speed | Fast | Slow |
| Security | Strong | Strong |
| Key Sharing | Difficult | Easy |
| Common Use | Data Encryption | Key Exchange |

---

# Cryptography in Cybersecurity

## Network Security

- HTTPS
- VPNs
- TLS

## Cloud Security

- Data Encryption
- Key Management

## Authentication

- Password Hashing
- MFA Systems

## Digital Forensics

- File Integrity Verification

## Secure Software Development

- Data Protection
- Secure Communications

---

# Key Takeaway

Modern cryptography relies on a combination of technologies:

- AES for Data Encryption
- RSA/ECC for Key Exchange
- SHA-256 for Integrity Verification
- Argon2/bcrypt for Password Storage
- TLS for Secure Communication

Together, these technologies form the foundation of modern cybersecurity, cloud security, secure software development, and secure communications.