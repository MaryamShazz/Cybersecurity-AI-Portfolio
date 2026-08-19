# What I Learned 

- Asymmetric encryption (Module 09) assumes you already have the correct public key for whoever you're talking to. **PKI** (Public Key Infrastructure) is the system that makes that assumption safe, by having a trusted third party vouch for the binding between a public key and an identity.
- Core PKI roles: **CA** (Certificate Authority issues and signs certificates), **RA** (Registration Authority verifies identity before a certificate is issued), **Certificate Repository** (stores/publishes certificates and revocation info), and **end entities** (the users, devices, or servers holding certificates).
- Working mechanism: an entity generates a key pair → submits the public key plus identity info to the RA/CA as a certificate request → the CA verifies identity and signs a certificate binding the public key to that identity → anyone who trusts the CA can then trust the certificate without independently verifying the identity themselves. This is the same mechanism behind a browser trusting an HTTPS site.
- Certificates can be compromised or become invalid before expiry. A **CRL** (Certificate Revocation List) is how a CA publishes which certificates should no longer be trusted.
- This module ties directly into Module 11: IPSec and SSL VPN can use certificates instead of preshared keys for authentication.
