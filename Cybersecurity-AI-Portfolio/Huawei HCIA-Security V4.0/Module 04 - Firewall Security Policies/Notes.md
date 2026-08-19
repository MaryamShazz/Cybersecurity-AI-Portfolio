# What I Learned - Module 04

- A Huawei firewall organizes interfaces into **security zones** (Trust, Untrust, DMZ, Local, or custom zones), each with a priority. Traffic between zones of different priorities is what a security policy governs; traffic within the same zone isn't inspected by default.
- A **security policy** matches traffic on source/destination zone, address, service, application, user, and time range, then permits or denies it. Rules are matched top to bottom — first match wins — so ordering matters.
- **Stateful inspection**: rather than checking every packet against the full policy list, the firewall builds a session table the first time a new connection is permitted, then just checks whether later packets belong to an existing session.
- **ASPF** (Application Specific Packet Filter) handles protocols like active-mode FTP that negotiate a separate data connection on a dynamic port — it watches the control channel and temporarily opens the port it expects to be used.
- Firewalls show up in a few standard roles depending on where they sit: perimeter gateway, boundary between internal zones (e.g. isolating a DMZ), or VPN termination point.
