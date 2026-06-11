# Blowfish

## Introduction

Blowfish is a symmetric-key block cipher developed by cryptographer Bruce Schneier in 1993.

It was designed as a fast, free, and secure alternative to existing encryption algorithms such as DES.

Unlike DES, Blowfish was not patented and could be used freely by anyone, which contributed to its popularity.

---

# Why Blowfish Was Created

## Problems with DES

DES suffered from several limitations:

- Small 56-bit Key Size
- Vulnerability to Brute Force Attacks
- Government Restrictions

Bruce Schneier designed Blowfish to provide:

- Stronger Security
- Faster Performance
- Free Public Use

---

# What Type of Encryption is Blowfish?

Blowfish is a:

- Symmetric Encryption Algorithm
- Block Cipher
- Secret Key Cryptography System

In symmetric encryption:

```text
Encryption Key = Decryption Key
```

The same key is used to encrypt and decrypt data.

---

# Blowfish Characteristics

## Block Size

Blowfish processes data in:

```text
64-bit Blocks
```

---

## Key Size

One of Blowfish's biggest advantages is its flexible key length.

Supported Key Sizes:

```text
32 Bits
↓
448 Bits
```

This flexibility allows organizations to choose stronger keys when needed.

---

# Blowfish Architecture

Blowfish uses a:

```text
Feistel Network
```

similar to DES.

---

## Number of Rounds

Blowfish performs:

```text
16 Rounds
```

of encryption.

---

# Blowfish Encryption Flow

```text
Plaintext
      ↓
Split Into
Left Half + Right Half
      ↓
16 Feistel Rounds
      ↓
Final Transformation
      ↓
Ciphertext
```

---

# Blowfish Internal Structure

## Step 1

Input Plaintext

```text
64 Bits
```

---

## Step 2

Split Data

```text
Left Half (32 Bits)

Right Half (32 Bits)
```

---

## Step 3

Perform 16 Encryption Rounds

Each round performs:

```text
XOR
Substitution
Permutation
Swapping
```

---

## Step 4

Final Swap

After the last round:

```text
Left ↔ Right
```

---

## Step 5

Generate Ciphertext

Encrypted output is produced.

---

# Blowfish Key Expansion

## Purpose

Before encryption begins, Blowfish generates several internal keys.

This process is called:

```text
Key Expansion
```

---

# Components Generated

## P-Array

Contains:

```text
18 Subkeys
```

Used during encryption rounds.

---

## S-Boxes

Contains:

```text
4 S-Boxes
```

Each containing:

```text
256 Entries
```

---

# Blowfish Round Function

Each round uses:

## XOR Operation

Combines data with a round key.

---

## Substitution

Uses S-Boxes.

Purpose:

```text
Confusion
```

Makes relationships between key and ciphertext difficult to determine.

---

## Permutation

Rearranges data.

Purpose:

```text
Diffusion
```

Spreads changes across the ciphertext.

---

# Blowfish Encryption Example

```text
Plaintext
    ↓
Split Data
    ↓
Round 1
    ↓
Round 2
    ↓
Round 3
    ↓
...
    ↓
Round 16
    ↓
Ciphertext
```

---

# Blowfish Decryption

Because Blowfish uses a Feistel Network:

```text
Encryption Process
=
Decryption Process
```

The only difference:

```text
Keys Used In Reverse Order
```

---

# Security of Blowfish

## Brute Force Resistance

Blowfish supports keys up to:

```text
448 Bits
```

making brute-force attacks extremely difficult.

---

## Cryptanalysis

No practical attack has successfully broken the full Blowfish algorithm.

The main weakness comes from:

```text
64-bit Block Size
```

rather than the encryption itself.

---

# Advantages of Blowfish

## Fast Encryption

Very efficient on older hardware.

---

## Strong Security

Large key sizes provide strong protection.

---

## Free and Open

No licensing restrictions.

---

## Flexible Key Length

Supports:

```text
32 - 448 Bits
```

---

## Well Tested

Extensively analyzed by cryptographers.

---

# Disadvantages of Blowfish

## Small Block Size

Only:

```text
64 Bits
```

Modern standards prefer:

```text
128 Bits
```

or larger.

---

## Slow Key Setup

Generating subkeys takes time.

This makes Blowfish less suitable when keys change frequently.

---

## Replaced by Newer Algorithms

Modern systems generally prefer:

- AES
- ChaCha20

---

# Blowfish vs DES

| Feature | DES | Blowfish |
|----------|----------|----------|
| Block Size | 64 Bits | 64 Bits |
| Key Size | 56 Bits | 32-448 Bits |
| Security | Weak | Strong |
| Performance | Moderate | Faster |
| Status | Obsolete | Legacy |

---

# Blowfish vs Triple DES

| Feature | Blowfish | Triple DES |
|----------|----------|----------|
| Block Size | 64 Bits | 64 Bits |
| Maximum Key | 448 Bits | 168 Bits |
| Performance | Faster | Slower |
| Security | Strong | Strong |
| Modern Usage | Limited | Limited |

---

# Blowfish vs AES

| Feature | Blowfish | AES |
|----------|----------|----------|
| Block Size | 64 Bits | 128 Bits |
| Key Size | 32-448 Bits | 128/192/256 Bits |
| Security | Strong | Stronger |
| Speed | Fast | Faster |
| Current Standard | No | Yes |
| Recommended Today | Rarely | Yes |

---

# Real-World Uses of Blowfish

## Password Managers

Historically used in:

- Password Storage Systems
- Credential Management Applications

---

## File Encryption

Used for:

- Secure File Storage
- Data Protection

---

## Backup Encryption

Used to protect archived data.

---

## Embedded Systems

Chosen because of:

- Low Resource Requirements
- Good Performance

---

# Blowfish Successor

## Twofish

Bruce Schneier later developed:

```text
Twofish
```

which improved upon Blowfish.

### Improvements

- Larger Block Size
- Better Performance
- Modern Design

---

# Current Status

Blowfish is still considered secure against direct attacks.

However, because of its:

```text
64-bit Block Size
```

it is no longer recommended for new systems.

Modern implementations typically use:

- AES-128
- AES-192
- AES-256
- ChaCha20

---

# Key Takeaway

Blowfish is a symmetric block cipher developed by Bruce Schneier to provide a secure, fast, and freely available alternative to DES. It uses a 16-round Feistel Network and supports key sizes from 32 to 448 bits. Although Blowfish remains cryptographically strong, its 64-bit block size has led most modern systems to adopt AES and ChaCha20 instead.