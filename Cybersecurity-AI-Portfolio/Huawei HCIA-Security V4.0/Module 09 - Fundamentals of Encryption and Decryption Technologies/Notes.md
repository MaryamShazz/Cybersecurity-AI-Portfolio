# What I Learned - Module 09

- **Symmetric encryption** uses the same key to encrypt and decrypt (e.g. AES). It's fast, so it's used for bulk data, but both sides need the same secret key, which makes secure key distribution the main challenge.
- **Asymmetric encryption** uses a key pair — public and private. Anything encrypted with one can only be decrypted with the other. This solves key distribution (the public key can be shared openly) but is computationally heavier, so it's not typically used for large volumes of data directly.
- Common real-world pattern: use asymmetric encryption to exchange a symmetric session key, then use that key for the actual bulk data. This is the same approach IPSec and SSL VPN use later in the course.
- **Hash algorithms** take an input of any size and produce a fixed-size output (a digest). They're one-way (not reversible) and collision-resistant (hard to find two inputs producing the same output). Used for integrity checking and, combined with a private key, digital signatures. Hashing and encryption are different tools — hashing is never meant to be reversed.
