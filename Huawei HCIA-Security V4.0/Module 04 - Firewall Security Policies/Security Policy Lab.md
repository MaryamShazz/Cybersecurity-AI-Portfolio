# Course Lab / Practical Exercise: Firewall Security Policy

This is the built in lab from Module 04, covering how a security policy is configured on a Huawei firewall, once through the CLI and once through the Web UI. Documented as a summary of what the exercise covers.

## What the Lab Covers

**CLI version**
1. Assigning interfaces to security zones (Trust for the internal LAN, Untrust for the external side).
2. Creating a security policy rule under `security policy`, matching source zone Trust, destination zone Untrust, a specific source address, and a service.
3. Setting the action to permit and committing the config.
4. Testing from an internal host to confirm matching traffic passes and non-matching traffic is dropped.

**Web UI version**
1. Rebuilding the same rule through the Web UI's visual rule builder.
2. Comparing the resulting configuration against the CLI version.

## Key Takeaway from the Module

The Web UI is really a front end generating the same underlying configuration as the CLI. Knowing the CLI matters more for troubleshooting and reading configs quickly; the Web UI is faster for day to day changes once the underlying logic is understood.
