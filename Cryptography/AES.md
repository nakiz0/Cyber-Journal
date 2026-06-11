# AES (Advanced Encryption Standard)

## Introduction

AES (Advanced Encryption Standard) is the most widely used symmetric encryption algorithm in the world today.

It was developed to replace DES and Triple DES because they became too weak or inefficient for modern security requirements.

AES was selected by the U.S. National Institute of Standards and Technology (NIST) in 2001 and has become the global standard for secure data encryption.

---

# What is AES?

AES is a:

- Symmetric Encryption Algorithm
- Block Cipher
- Secret Key Cryptography System

In symmetric encryption:

```text
Encryption Key = Decryption Key
```

The same key is used to encrypt and decrypt data.

---

# Why AES Was Created

## Problems with DES

DES suffered from:

- Small Key Size (56-bit)
- Vulnerability to Brute Force Attacks

---

## Problems with Triple DES

Triple DES improved security but introduced:

- Slower Performance
- High Computational Cost
- Outdated Architecture

---

## Solution

NIST launched a competition to find a replacement.

The winning algorithm was:

```text
Rijndael
```

which became:

```text
AES
```

---

# AES Characteristics

## Block Size

AES always operates on:

```text
128-bit Blocks
```

Unlike DES:

```text
DES = 64 Bits
AES = 128 Bits
```

---

# AES Key Sizes

AES supports three key lengths.

## AES-128

```text
128-bit Key
```

Rounds:

```text
10 Rounds
```

---

## AES-192

```text
192-bit Key
```

Rounds:

```text
12 Rounds
```

---

## AES-256

```text
256-bit Key
```

Rounds:

```text
14 Rounds
```

---

# Why Different Key Sizes?

Larger keys provide:

- Stronger Security
- More Possible Key Combinations

However:

- More Processing Required
- Slightly Slower Encryption

---

# AES Encryption Flow

```text
Plaintext
      ↓
Key Expansion
      ↓
Initial Round
      ↓
Multiple Encryption Rounds
      ↓
Final Round
      ↓
Ciphertext
```

---

# AES Architecture

AES does not use a Feistel Network like DES.

Instead it uses:

```text
Substitution-Permutation Network (SPN)
```

This structure provides:

- Confusion
- Diffusion

which are essential cryptographic properties.

---

# AES Encryption Process

# Step 1: Key Expansion

## Purpose

Generate round keys from the original key.

Example:

```text
Original Key
      ↓
Round Keys Generated
      ↓
Used Throughout Encryption
```

---

# Step 2: Initial Round

## AddRoundKey

Plaintext is XORed with the first round key.

```text
Data XOR Key
```

This is the first protection layer.

---

# Step 3: Main Rounds

Each round contains four operations.

---

## SubBytes

### Purpose

Substitutes bytes using a lookup table called:

```text
S-Box
```

### Purpose

Provides:

- Confusion
- Non-Linearity

making attacks more difficult.

---

## ShiftRows

### Purpose

Rows of data are shifted.

Example:

```text
Row 1 → Shift Left 1
Row 2 → Shift Left 2
Row 3 → Shift Left 3
```

### Purpose

Improves diffusion.

---

## MixColumns

### Purpose

Columns are mathematically mixed.

### Benefits

- Data Spreading
- Stronger Encryption

---

## AddRoundKey

### Purpose

Round key is XORed with current data.

```text
Data XOR Round Key
```

---

# Final Round

The final round removes:

```text
MixColumns
```

and performs:

```text
SubBytes
ShiftRows
AddRoundKey
```

---

# AES Decryption Process

Decryption reverses encryption.

```text
Ciphertext
      ↓
Inverse ShiftRows
      ↓
Inverse SubBytes
      ↓
Inverse MixColumns
      ↓
Original Plaintext
```

---

# AES Visualization

```text
Plaintext
     ↓
AddRoundKey
     ↓
SubBytes
     ↓
ShiftRows
     ↓
MixColumns
     ↓
AddRoundKey
     ↓
Repeat
     ↓
Ciphertext
```

---

# AES Security

## Brute Force Resistance

AES is extremely resistant to brute-force attacks.

### AES-128

Possible Keys:

```text
2^128
```

### AES-256

Possible Keys:

```text
2^256
```

These numbers are so large that brute forcing them is practically impossible using current technology.

---

# Advantages of AES

## Strong Security

AES remains secure against known practical attacks.

---

## Fast Performance

Works efficiently on:

- CPUs
- Smartphones
- Servers
- Embedded Devices

---

## Global Standard

Used worldwide by:

- Governments
- Banks
- Cloud Providers
- Security Applications

---

## Hardware Acceleration

Modern processors include:

```text
AES-NI
```

which speeds up encryption significantly.

---

# Disadvantages of AES

## Key Management

The encryption key must be protected.

If an attacker obtains the key:

```text
Encryption becomes useless.
```

---

## Symmetric Key Problem

The same key must be shared securely between parties.

This is why AES is often combined with:

- RSA
- ECC
- Diffie-Hellman

for secure key exchange.

---

# AES in Real Life

## HTTPS

Used to encrypt:

```text
Browser ↔ Website
```

communications.

---

## VPNs

Used by:

- OpenVPN
- IPSec
- WireGuard (ChaCha20 Alternative)

---

## Wi-Fi Security

Used in:

```text
WPA2
WPA3
```

---

## Cloud Security

Used by:

- AWS
- Azure
- Google Cloud

for data encryption.

---

## Disk Encryption

Examples:

- BitLocker
- VeraCrypt
- LUKS

---

# AES vs DES

| Feature | DES | AES |
|----------|----------|----------|
| Block Size | 64 Bits | 128 Bits |
| Key Size | 56 Bits | 128/192/256 Bits |
| Security | Weak | Very Strong |
| Speed | Slower Modern Usage | Fast |
| Status | Obsolete | Industry Standard |
| Rounds | 16 | 10/12/14 |

---

# AES vs Triple DES

| Feature | AES | Triple DES |
|----------|----------|----------|
| Block Size | 128 Bits | 64 Bits |
| Security | Higher | Lower |
| Performance | Faster | Slower |
| Key Sizes | 128/192/256 | 112/168 |
| Modern Usage | Yes | Legacy |
| Recommended | Yes | No |

---

# Common AES Modes

## ECB (Electronic Codebook)

### Characteristics

- Simplest Mode
- Not Recommended

### Weakness

Identical plaintext blocks produce identical ciphertext blocks.

---

## CBC (Cipher Block Chaining)

### Characteristics

- More Secure Than ECB
- Uses Initialization Vector (IV)

---

## CTR (Counter Mode)

### Characteristics

- Fast
- Parallel Processing

---

## GCM (Galois/Counter Mode)

### Characteristics

- Encryption
- Authentication

### Widely Used In

- HTTPS
- TLS
- Cloud Security

---

# Key Takeaway

AES (Advanced Encryption Standard) is the world's most widely used symmetric encryption algorithm. It was designed to replace DES and Triple DES and provides strong security, excellent performance, and broad industry adoption. Modern technologies such as HTTPS, VPNs, Wi-Fi security, cloud platforms, and disk encryption all rely heavily on AES to protect sensitive information.