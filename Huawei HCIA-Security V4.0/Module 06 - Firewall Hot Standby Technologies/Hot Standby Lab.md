# Course Lab / Practical Exercise: Firewall Hot Standby

## What the Lab Covers

**CLI**
1. Cabling two firewalls together with a dedicated HRP heartbeat link.
2. Configuring matching VRRP virtual IPs on the corresponding interfaces of both devices.
3. Grouping the VRRP instances under VGMP so they fail over together.
4. Enabling HRP and confirming active/standby roles, with the standby syncing session and config state from the active device.
5. Simulating a failure by shutting down the active firewall's link and confirming the standby takes over the virtual IP while keeping existing sessions alive.

**Web UI**
1. Repeating the same setup through the Web UI's hot standby configuration section.
2. Checking the HRP status page to confirm both devices agree on which one is active.

## Key Takeaway from the Module

The failover test is the point of the exercise: a ping barely pausing (instead of dropping outright) when the active firewall goes down demonstrates why the heartbeat link between the two firewalls isn't optional, it's what keeps the standby actually usable rather than just present.
