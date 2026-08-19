# What I Learned - Module 02

- OSI breaks networking into seven layers; TCP/IP collapses that into four. The course used both, since some firewall concepts (session tables) map more naturally to TCP/IP, while others (application-layer inspection) fit the OSI lens better.
- **Application Layer** — where protocols users interact with live (HTTP, DNS, FTP). Also where a lot of modern firewall inspection happens, since so much traffic is tunneled over HTTP/HTTPS.
- **Transport Layer** — TCP/UDP; where the firewall builds its session table, tracking ports and connection state.
- **Network Layer** — IP addressing and routing; where security zones and NAT operate.
- **Data Link Layer** — MAC addressing and switching; less of a focus for firewall policy but still relevant to things like ARP spoofing.
- Common network devices covered: switches, routers, and firewalls. The distinction the course drew: routers/switches are built to move traffic efficiently, while a firewall is built to inspect traffic and decide whether it should move at all.
