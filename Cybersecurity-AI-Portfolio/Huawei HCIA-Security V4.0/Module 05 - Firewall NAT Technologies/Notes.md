# What I Learned - Module 05

- NAT originally solved IPv4 address exhaustion by translating private internal addresses to a smaller pool of public addresses at the network edge. A side benefit is that it also hides internal addressing from the outside world.
- **Source NAT** rewrites the source address (and usually port) of outbound traffic — typically many internal addresses to one or a few public addresses. The everyday case: internal users browsing the internet.
- **Destination NAT** rewrites the destination address of inbound traffic — commonly used to publish an internal server to a public-facing address.
- **Bidirectional NAT** translates both source and destination on the same session — used when two networks with overlapping private address ranges need to communicate.
- **NAT Server** is a specific, persistent form of destination NAT for publishing a server. **NAT ALG** (Application Level Gateway) rewrites IP/port data embedded inside application payloads for protocols a plain NAT rule can't see into — the same problem ASPF solves in Module 04.
- Important distinction: NAT only rewrites addresses. A security policy still has to separately permit the (translated) traffic, or it's dropped regardless of the NAT rule.
