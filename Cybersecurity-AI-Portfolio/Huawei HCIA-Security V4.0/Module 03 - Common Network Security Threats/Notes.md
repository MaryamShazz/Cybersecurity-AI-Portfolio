# What I Learned - Module 03

The module divides an enterprise network into four areas to reason about where defenses are actually needed:

- **Communication network** — the links and infrastructure carrying traffic between locations. Threats: interception, tampering in transit, availability (link failures, DDoS). Solutions: encryption (VPNs), redundancy.
- **Zone borders** — the boundary between security zones (internal network vs. internet, DMZ vs. everything else). This is firewall territory: security policies, NAT, IPS.
- **Computing environment** — servers, endpoints, and applications. Closer to host-based security: patching, antivirus, hardening. The firewall controls what reaches these systems but can't fix a vulnerable application on its own.
- **Management center** — the systems used to manage everything else (e.g. the firewall's own management interface). If this is compromised, an attacker can reconfigure defenses rather than just bypass one. This is why restricting management access and using SSH/HTTPS instead of Telnet/HTTP matters.

This four-area framing is used as a reference point across the rest of the course — NAT and security policy work fall under zone borders, AAA and PKI touch the management center, and hot standby is about keeping the communication network available.
