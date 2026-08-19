# Course Lab / Practical Exercise: Firewall Login

This is the built-in lab from Module 02 of the course, covering how to reach a Huawei USG firewall through every access method the platform provides. Documented here as a summary of what the exercise covers, not as an independent setup.

## What the Lab Covers

1. **Console login via PuTTY** — connecting to the firewall's console port through a serial session, the fallback method when the device has no network config yet.
2. **Getting familiar with commands** — the CLI's view modes (user view, system view, interface view), moving between them, and using the `?` help system for command completion.
3. **Telnet login** — configuring the firewall to accept Telnet and logging in over the network. The course notes that Telnet sends everything in plaintext, so it isn't something you'd leave enabled on a production device.
4. **SSH login** — the encrypted alternative to Telnet, the one you'd actually want for day-to-day remote access.
5. **Default Web UI login** — logging into the firewall's out-of-the-box web management interface with default credentials, then the initial setup wizard.
6. **Web UI after configuration** — logging in again once the management IP and credentials have been changed, to see how access changes for a real deployment.

## Key Takeaway from the Module

Each access method comes with its own security trade-off: console access is safest but needs physical presence, Telnet is convenient but insecure, and SSH/HTTPS Web UI are the ones you'd rely on for secure remote management.
