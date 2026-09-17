---
type: observation
domain: [cybersecurity, web-hosting]
confidence: 0.85
sources: 1
entities: [Acronis, cPanel, WHM, Plesk, CVE-2026-87886]
motifs: [insecure-file-permissions, supply-chain-plugin-risk]
refs: ['https://thehackernews.com/2026/09/acronis-cpanel-backup-plugin.html']
---
# CVE-2026-87886: Acronis cPanel/WHM Backup plugin local privilege escalation exploited in the wild

Acronis warned in September 2026 that CVE-2026-87886 (CVSS 7.8), a local privilege escalation flaw caused by insecure file permissions in its Backup plugin for cPanel and Web Host Manager, has been exploited in the wild. Affected: Acronis Backup plugin for cPanel & WHM (Linux) before build 1.9.3.1021, fixed in 1.9.3 HF3; and Acronis Backup extension for Plesk (Linux) before build 1.8.11.638. Exploitation lets a low-privileged attacker escalate permissions on the Linux host and potentially run arbitrary code, affecting application confidentiality and integrity. Acronis advised installing the update immediately.
