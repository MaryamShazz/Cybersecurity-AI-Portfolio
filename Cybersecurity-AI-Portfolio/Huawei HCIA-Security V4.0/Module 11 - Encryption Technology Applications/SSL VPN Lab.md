# Course Lab / Practical Exercise 2: SSL VPN

This is the built-in lab from Module 11, covering SSL VPN configuration on a Huawei firewall's simulated environment. Documented as a summary of what the exercise covers.

## What the Lab Covers

1. Enabling the SSL VPN feature and configuring a virtual gateway with an HTTPS listening address/port.
2. Creating a local user account for remote access, assigned to an SSL VPN authentication domain.
3. Defining the resources a remote user should reach after connecting (specific internal servers/subnets, not the whole network).
4. Configuring the SSL VPN policy tying the user/domain to those resources.
5. Connecting from a simulated remote client through a browser to the firewall's SSL VPN portal, logging in, and confirming access is limited to the defined resources.
6. Attempting to reach a resource that wasn't explicitly granted, to confirm it's correctly blocked.

## Key Takeaway from the Module

The contrast with the IPSec lab is the point of pairing these two: IPSec needs matching configuration on both firewalls and effectively bridges two networks together, while SSL VPN needs almost no client-side setup, just a browser and credentials, and is scoped to specific resources by default. This is why SSL VPN tends to be the choice for individual remote workers, while IPSec fits connecting two fixed sites.
