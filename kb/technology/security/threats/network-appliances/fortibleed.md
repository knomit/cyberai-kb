---
type: observation
domain: [security, vulnerability, network]
confidence: 0.83
sources: 2
entities: [FortiBleed, FortiGate, FortiOS, FortigateSniffer, SOCRadar, CISA, Fortinet]
refs: ['https://thehackernews.com/2026/06/cisa-warns-fortinet-customers-as.html', 'https://thehackernews.com/2026/06/fortibleed-targeted-fortigate-firewalls.html']
---
# FortiBleed: Russian-speaking IAB credential-harvesting campaign against FortiGate firewalls

FortiBleed is a large-scale, financially motivated credential-harvesting campaign attributed to a Russian-speaking initial access broker (IAB), active since February 2026 and targeting over 430,000 FortiGate firewalls globally; reporting ties it to roughly 110 million harvested credentials, with 86,644 devices assessed as compromised as of June 19, 2026. CISA urged Fortinet/FortiGate customers to secure their appliances. Per SOCRadar, the operation collects credential lists, scans for exposed services, brute-forces accessible systems, and deploys a Golang-based tool, FortigateSniffer (Windows and Unix variants), which abuses the FortiOS built-in 'diagnose sniffer packet' diagnostic command to passively capture cleartext and hashed authentication traffic; the actors then crack, validate, and reuse credentials against Active Directory and other exposed services. Of compromised credentials, generic admin accounts (35%) and built-in Fortinet system accounts (28.3%) made up the majority (org-specific 36.7%), pointing to widespread failure to rename default accounts or rotate factory credentials.
