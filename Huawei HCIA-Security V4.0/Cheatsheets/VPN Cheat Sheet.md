# VPN Cheat Sheet

| Type | Layer | Encrypts? | Typical Use |
|---|---|---|---|
| GRE | Network | No | Tunneling different traffic types / overlapping addresses; usually paired with IPSec |
| IPSec | Network | Yes | Site to site VPNs, full network layer access, transport or tunnel mode |
| L2TP | Data link | No (needs IPSec) | Remote access, usually as L2TP/IPSec |
| SSL VPN | Application/Transport | Yes | Remote access via browser, minimal client setup, resource scoped access |

## IPSec Modes
- **Transport mode** : encrypts payload only, original IP header kept → host to host
- **Tunnel mode** : encrypts entire original packet, new IP header added → site to site

## IPSec Key Building Blocks
- **IKE** : negotiates the security association, derives shared keys (preshared key or certificate based)
- **IKE proposal** : must match exactly on both peers (encryption algorithm, authentication algorithm, DH group) or negotiation fails
- **IPSec policy** : ties the IPSec proposal to "interesting traffic" (the source/destination subnets that go through the tunnel)
- Security policy must still separately permit the tunnel traffic

## Quick Troubleshooting Reminder
If an IPSec tunnel won't come up, check the IKE proposal parameters match on both sides first, before anything else, mismatched DH group/encryption/auth algorithm is the most common cause of a failed negotiation.
