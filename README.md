# TryHackMe - Cryptography Concepts

## Overview
This repository contains my notes and practical examples from the TryHackMe Cryptography Concepts room.

## Learning Objectives

- Understand the role of cryptography in cybersecurity
- Learn symmetric and asymmetric encryption
- Explore hashing functions
- Understand digital signatures and certificates
- Identify common cryptographic vulnerabilities

## Topics Covered

### 1. Symmetric Encryption
- Uses a single key for encryption and decryption
- Fast and efficient
- Example: AES

### 2. Asymmetric Encryption
- Uses public and private key pairs
- Supports secure key exchange
- Example: RSA

### 3. Hashing
- One-way transformation of data
- Used for integrity verification
- Examples: SHA-256, SHA-512

### 4. Digital Signatures
- Verify authenticity and integrity
- Uses private key signing and public key verification

### 5. Public Key Infrastructure (PKI)
- Certificates
- Certificate Authorities (CAs)
- Trust chains

## Practical Python Examples

### SHA-256 Hashing

```python
import hashlib

message = "TryHackMe Cryptography Concepts"

hash_value = hashlib.sha256(message.encode()).hexdigest()

print("SHA-256:", hash_value)
```

### AES Encryption (PyCryptodome)

```python
from Crypto.Cipher import AES
from Crypto.Random import get_random_bytes

key = get_random_bytes(16)
cipher = AES.new(key, AES.MODE_EAX)

data = b"Hello Cryptography"

ciphertext, tag = cipher.encrypt_and_digest(data)

print("Encrypted:", ciphertext.hex())
```

### RSA Key Generation

```python
from Crypto.PublicKey import RSA

key = RSA.generate(2048)

private_key = key.export_key()
public_key = key.publickey().export_key()

print("Private Key Generated")
print("Public Key Generated")
```

## Key Takeaways

- Cryptography protects confidentiality, integrity, and authenticity.
- Strong encryption relies on proper key management.
- Hashing is not encryption.
- Digital signatures provide non-repudiation.
- Cryptography is a foundational cybersecurity skill.

## Platform

Completed on TryHackMe as part of my cybersecurity learning journey.
