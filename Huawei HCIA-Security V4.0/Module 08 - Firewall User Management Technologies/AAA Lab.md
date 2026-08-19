# Course Lab / Practical Exercise: User Management

This is the built-in lab from Module 08, covering AAA-based user authentication on a Huawei firewall. Documented as a summary of what the exercise covers.

## What the Lab Covers

1. Creating a user organization structure with a couple of user groups representing different departments.
2. Adding local user accounts under those groups with individual credentials.
3. Configuring an authentication domain to tie the users to.
4. Writing an authentication policy so traffic from a specific zone requires the user to authenticate before it's matched against the rest of the security policies.
5. Testing from a client machine: traffic is blocked with an authentication prompt until logging in as one of the test users, after which it matches the security policy tied to that user's group.

## Key Takeaway from the Module

The exercise draws a clear line between IP-based and identity-based policy: once a user has to authenticate, the firewall can apply different rules to two people on the exact same subnet — a more realistic access-control model for an office environment where IP addresses get reassigned constantly.
