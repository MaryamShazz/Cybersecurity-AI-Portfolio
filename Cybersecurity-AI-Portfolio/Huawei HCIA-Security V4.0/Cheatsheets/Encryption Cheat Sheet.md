# Encryption Cheat Sheet

## Symmetric Encryption
- Same key encrypts and decrypts (e.g. AES)
- Fast → used for bulk data
- Weakness: securely distributing the shared key

## Asymmetric Encryption
- Key pair: public + private
- Public key can be shared openly, only the matching private key can decrypt
- Solves key distribution, but computationally heavier → not used for large data volumes directly

## Common Real-World Pattern
Asymmetric encryption exchanges a symmetric session key → symmetric encryption handles the actual bulk data. This is how IPSec and SSL VPN both work under the hood.

## Hash Algorithms
- Fixed-size output from any input size
- One-way (not reversible)
- Collision-resistant (hard to find two inputs with the same output)
- Used for: integrity checking, and (combined with a private key) digital signatures
- Not the same as encryption — hashing is never meant to be reversed
