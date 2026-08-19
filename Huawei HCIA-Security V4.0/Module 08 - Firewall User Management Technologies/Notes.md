# What I Learned 

- **AAA** breaks into three distinct jobs: **Authentication** (confirming who a user is), **Authorization** (deciding what they're allowed to do), and **Accounting** (logging what they did, for auditing).
- The firewall organizes users into a hierarchy (organizations and user groups) rather than a flat list, so policies can reference a group instead of individual accounts, which scales better across departments.
- Typical authentication flow: traffic hits a policy requiring authentication → the firewall challenges the user → the user authenticates (locally, or against an external server) → traffic is then matched against policies tied to the user's identity or group instead of just their IP.
- Authentication policies define which traffic actually needs identity verification, not everything has to require it, so it's a deliberate decision about where identity based control matters versus where IP/zone based policy is enough.
- Configuring this involves setting up local user accounts/groups, an authentication domain, and an authentication policy tying specific traffic to the requirement to authenticate first.
