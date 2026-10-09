---
type: observation
domain: [security, vulnerability]
confidence: 0.8
sources: 1
entities: [SonicWall, SMA1000, CVE-2026-102255]
refs: ['https://thehackernews.com/2026/10/sonicwall-patches-cvss-100-pre.html']
---
# SonicWall SMA1000 pre-auth SSRF CVE-2026-102255 (CVSS 10.0) patched

SonicWall released hotfixes (advisory dated 2026-10-06) for four flaws in SMA1000 remote-access appliances (models 6210, 7210, 8200v). The most severe, CVE-2026-102255, is a pre-authentication SSRF in the WorkPlace portal rated CVSS 10.0, letting an unauthenticated attacker reach internal functionality. SonicWall says it has no evidence of exploitation of any of the four flaws. Apply the hotfixes; absence of known exploitation is not a reason to delay. Distinct from earlier exploited SMA1000 zero-days.
