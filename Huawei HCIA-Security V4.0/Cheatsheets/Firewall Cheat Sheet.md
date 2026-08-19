# Firewall Cheat Sheet

## Security Zones
- Default zones: Local, Trust, DMZ, Untrust (each with a priority)
- Traffic within the same zone: not inspected by default
- Traffic between zones: matched against security policy

## Security Policy
- Match criteria: source/destination zone, address, service, application, user, time range
- Matched top to bottom, first match wins → order specific rules above general ones
- Default action if nothing matches: deny

## Stateful Inspection
- Session table built on first permitted packet of a new connection
- Return traffic matched against session table, not re-evaluated against policy from scratch

## ASPF
- Watches control-channel traffic for protocols that negotiate dynamic ports (e.g. active FTP)
- Temporarily opens the required port based on what it observes

## Quick CLI Reference
```
system-view
security-zone name <zone>
security-policy
 rule name <rule-name>
  source-zone <zone>
  destination-zone <zone>
  source-address <address/address-set>
  destination-address <address/address-set>
  service <service>
  action permit
```
