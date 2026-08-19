# PKI Cheat Sheet

## Core Roles
- **CA (Certificate Authority)** : issues and signs certificates
- **RA (Registration Authority)** : verifies identity before a certificate is issued
- **Certificate Repository** : stores/publishes issued certificates and revocation info
- **End entity** : the user/device/server holding the certificate

## Basic Flow
1. Entity generates a key pair
2. Public key + identity info submitted to RA/CA as a certificate request
3. CA verifies identity, signs a certificate binding the public key to that identity
4. Anyone trusting the CA can trust the certificate (and the public key inside it) without verifying the identity themselves

## Revocation
- Certificates can become invalid before expiry (compromise, etc.)
- **CRL (Certificate Revocation List)** : published by the CA to flag certificates that should no longer be trusted

## Why It Matters for VPNs
- IKE (used by IPSec) can authenticate using certificates instead of a preshared key
- Certificate based auth scales better than pre-shared keys once you're past a handful of VPN peers
