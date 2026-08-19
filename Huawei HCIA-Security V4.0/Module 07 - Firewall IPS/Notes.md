# What I Learned 

- The module distinguishes an **IDS** (Intrusion Detection System : detects and alerts) from an **IPS** (Intrusion Prevention System : detects and actively blocks). A Huawei firewall's IPS function sits inline with traffic, so it can drop malicious traffic in real time.
- IPS works off signature databases : patterns matching known attack traffic (exploit attempts, scanning behavior, known malware C2 traffic). Configuring it means choosing which signature categories to enable, setting an action (alert/block) per severity level, and applying the resulting profile to a security policy.
- IPS is really an extension of the security policy work from Module 04: the security policy decides what traffic is allowed through; the IPS profile decides what happens to allowed traffic that still looks malicious.
- **Antivirus** on the firewall inspects file transfers (HTTP, FTP, SMTP) against a virus signature database and can block or alert on matches. It only catches known threats — it's an additional layer, not a substitute for endpoint antivirus.
