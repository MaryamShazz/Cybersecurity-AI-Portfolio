# Course Lab / Practical Exercise 1: Site to Site IPSec VPN

## What the Lab Covers

1. Two firewalls representing two separate sites, each with an internal (Trust) network and a link out to a simulated public network (Untrust).
2. Configuring an IKE proposal on both firewalls (encryption algorithm, authentication algorithm, DH group), matched on both ends, IKE negotiation fails if the two sides don't agree on the same parameters.
3. Setting a preshared key for IKE authentication between the two peers.
4. Defining an IPSec proposal and referencing it in an IPSec policy tied to "interesting traffic" the source/destination subnets that should go through the tunnel.
5. Applying the IPSec policy to the outbound interface on both firewalls.
6. Adding security policies to permit the tunnel traffic, IPSec doesn't bypass the security policy, it still needs to be explicitly allowed (the same point made in Module 04).
7. Testing connectivity between the two sites' internal networks and confirming, via the firewall's IPSec monitoring page, that a security association (SA) is established.

## Key Takeaway from the Module

IPSec is strict about both ends agreeing on every IKE parameter before a tunnel comes up at all very different from a basic security policy, where a small mismatch just changes what's matched rather than breaking the whole connection.
