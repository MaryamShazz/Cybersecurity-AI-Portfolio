# What I Learned - Module 06

Three protocols work together here, and keeping their roles separate is the key to understanding this module:

- **VRRP** (Virtual Router Redundancy Protocol) lets two or more devices share a single virtual IP address. Hosts point to the virtual IP as their gateway; VRRP decides which physical device currently answers for it, and the standby takes over if the active device fails.
- **VGMP** (VRRP Group Management Protocol) groups all of a firewall's VRRP instances together so they fail over as one unit instead of independently — since a firewall usually has multiple interfaces, each potentially running its own VRRP instance.
- **HRP** (Huawei Redundancy Protocol) keeps the standby firewall in sync with the active one, syncing the session table, configuration, and connection status. Without this, a failover would work at the routing level, but the standby wouldn't know what sessions were active and existing connections would still drop.

Summary: VRRP handles who owns the IP, VGMP makes interfaces fail over together, and HRP makes sure the standby has the state it needs for the failover to be seamless rather than just "the IP moved but every connection broke."
