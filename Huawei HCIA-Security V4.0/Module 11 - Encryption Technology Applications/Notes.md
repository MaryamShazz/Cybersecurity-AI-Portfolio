# What I Learned 

- A VPN extends a private network across a public one (usually the internet) while keeping traffic private and, depending on the type, authenticated.
- **GRE VPN** tunnels traffic by wrapping one packet inside another, but doesn't encrypt anything on its own, it's often paired with IPSec, which handles the encryption GRE lacks.
- **IPSec VPN** operates at the network layer and provides encryption and authentication for IP traffic, in two modes: **transport mode** (encrypts the payload only, keeps the original IP header host to host) and **tunnel mode** (encrypts the entire original packet inside a new IP header used for site to site VPNs). Key exchange happens through **IKE**, which negotiates the security association using a preshared key or, tying back to Module 10, certificates.
- **L2TP VPN** tunnels at layer 2 but, like GRE, doesn't encrypt on its own almost always paired with IPSec (L2TP/IPSec), typically for remote access.
- **SSL VPN** operates at a higher layer and is what most modern remote access VPNs are built on, since it can work through a browser or a lightweight client without network layer configuration on the client device. It typically exposes specific applications/resources rather than full network access.
- This module is the payoff for Modules 09 and 10, every VPN type here depends on the encryption/hashing fundamentals and the PKI trust model covered earlier.
