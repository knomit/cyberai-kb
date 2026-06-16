---
type: synthesis
domain: [security]
confidence: 0.8
sources: 1
entities: [Oracle PeopleSoft, Splunk, Palo Alto Networks, Check Point, ShinyHunters, CISA]
refs: [kb/technology/security/threat-actors/shinyhunters/ee9d7f8c.md, kb/technology/security/vulnerabilities/critical-rce/4e34e308.md, kb/technology/security/vulnerabilities/vpn/bf813749.md, kb/technology/security/vulnerabilities/vpn/b819bfdf.md]
---
# Mid-2026 wave of actively-exploited auth-bypass flaws in enterprise edge and infrastructure software

Across early-to-mid June 2026, multiple high/critical vulnerabilities in widely-deployed enterprise edge and infrastructure products were disclosed as actively exploited or imminently weaponizable, frequently rooted in missing or bypassable authentication: Oracle PeopleSoft CVE-2026-35273 (CVSS 9.8, exploited by ShinyHunters/UNC6240), Splunk Enterprise CVE-2026-20253 (CVSS 9.8, unauthenticated RCE via an unauthenticated PostgreSQL sidecar), Palo Alto PAN-OS GlobalProtect CVE-2026-0257 (auth bypass, exploited from May 17), and Check Point Remote Access VPN CVE-2026-50751. The pattern: internet-facing VPN/remote-access portals and enterprise back-office platforms remain the highest-value targets, the patch-to-exploit gap is short, and CISA KEV deadlines track these closely. Practical implication: prioritize patching internet-exposed identity/VPN/admin endpoints first.
