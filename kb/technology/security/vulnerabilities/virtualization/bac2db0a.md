---
type: observation
domain: [security, apt, ransomware]
confidence: 0.85
sources: 1
entities: [VMware vCenter, CVE-2026-59310, Babuk, QUIRSO]
refs: ['https://thehackernews.com/2026/08/suspected-china-nexus-actor-exploits.html']
---
# CVE-2026-59310: VMware vCenter directory traversal exploited by suspected China-nexus APT

CVE-2026-59310 (CVSS 9.8) is a directory-traversal vulnerability in VMware vCenter Server allowing arbitrary code execution. A suspected China-nexus APT is assessed to be behind in-the-wild exploitation. In at least one compromised instance the attack deployed a backdoor and a reverse SSH binary, ending in Babuk-derived ransomware. Investigators (QUIRSO) assess the ransomware was likely a smokescreen to hinder forensic analysis by encrypting evidence rather than the primary objective.
