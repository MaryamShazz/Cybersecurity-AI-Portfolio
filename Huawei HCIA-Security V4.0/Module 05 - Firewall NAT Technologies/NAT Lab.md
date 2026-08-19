# Course Lab / Practical Exercise: Firewall NAT Server and Source NAT

## What the Lab Covers

**Source NAT (CLI)**
1. Setting up a NAT address pool using a public IP range.
2. Creating a source NAT policy matching outbound traffic from the internal zone, translated to the address pool.
3. Verifying from an internal host that outbound traffic shows the translated address externally.

**Source NAT (Web)**
1. Rebuilding the same rule through the Web UI's NAT policy section.

**NAT Server and Source NAT (CLI)**
1. Adding a NAT Server rule mapping a public IP/port to an internal server's private IP/port.
2. Keeping the source NAT rule active alongside it, so internal users can still reach the internet while the server is published outward.
3. Testing access to the internal server from an external side host.

**NAT Server and Source NAT (Web)**
1. Repeating the same setup through the Web UI.

## Key Takeaway from the Module

NAT and security policy are separate layers: NAT rewrites addresses, but the security policy still has to explicitly permit that traffic. A NAT Server rule alone doesn't grant access, the exercise flags this as a common configuration mistake.
