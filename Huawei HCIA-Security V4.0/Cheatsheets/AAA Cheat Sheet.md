# AAA Cheat Sheet

## The Three A's
- **Authentication** — confirming identity (who are you)
- **Authorization** — what you're allowed to do
- **Accounting** — logging what you did

## Setup Order (Local Auth)
1. Create user groups / organization structure
2. Create local user accounts, assign to groups
3. Configure an authentication domain
4. Write an authentication policy: which traffic requires authentication before it's matched against security policy

## Why Identity-Based Policy Matters
- IP-based policy can't distinguish two people on the same subnet
- User/group-based policy can apply different rules to different people regardless of IP
- Scales better than managing individual IP-based rules per person

## High-Level Flow
Traffic hits policy requiring auth → firewall challenges user → user authenticates (local or external server) → traffic re-evaluated against policies tied to user/group identity
