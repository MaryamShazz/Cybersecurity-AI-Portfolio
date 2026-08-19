# Course Lab / Practical Exercise: Configuring Intrusion Prevention and Antivirus

This is the built-in lab from Module 07, covering IPS and antivirus profile configuration on a Huawei firewall. Documented as a summary of what the exercise covers.

## What the Lab Covers

1. Enabling the IPS signature database and reviewing the available signature categories.
2. Building an IPS profile: action set to block for high-severity signatures, alert-only for lower-severity ones.
3. Applying the IPS profile to a security policy, so traffic already permitted by zone/service is also inspected for known attack patterns.
4. Repeating a similar process for antivirus: enabling the antivirus profile, setting the action for detected files, and applying it to a policy.
5. Checking logs after generating test traffic to confirm the IPS and antivirus profiles are matching and logging correctly.

## Key Takeaway from the Module

Neither feature is "set and forget" — the action level chosen (blocking vs. alerting) has real consequences either way, and a profile only does anything once it's attached to a security policy. This reinforces security policy as the backbone the rest of the firewall's features hang off of.
