# NAT Cheat Sheet

| Type | Rewrites | Typical Use |
|---|---|---|
| Source NAT | Source address of outbound traffic | Internal users reaching the internet |
| Destination NAT | Destination address of inbound traffic | Publishing an internal server |
| Bidirectional NAT | Both source and destination | Overlapping address spaces between two networks |
| NAT Server | Persistent destination NAT mapping | Long term server publishing |
| NAT ALG | Embedded IP/port data inside application payloads | Protocols like FTP that break under plain NAT |

## Reminder
NAT only rewrites addresses, it does **not** grant access by itself. A matching security policy still has to permit the (translated) traffic, or it gets dropped regardless of the NAT rule.

## Quick CLI Reference
```
nat address-group <group-name>
 mode pat
 section 0 <start-ip> <end-ip>

nat-policy
 rule name <rule-name>
  source-zone trust
  destination-zone untrust
  source-address <address>
  action source-nat address-group <group-name>
```
