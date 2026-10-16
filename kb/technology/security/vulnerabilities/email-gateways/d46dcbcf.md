---
type: observation
domain: [security, vulnerability]
confidence: 0.8
sources: 1
entities: [Cisco, Cisco Secure Email Gateway, AsyncOS, CVE-2026-76519]
refs: ['https://thehackernews.com/2026/10/cisco-warns-of-active-attacks.html']
---
# Cisco Secure Email Gateway critical pre-auth file-write flaw actively exploited (CVE-2026-76519)

Cisco warned (advisory 2026-10-14) of active exploitation of CVE-2026-76519 in Cisco Secure Email Gateway: an unauthenticated sender can write files to the appliance OS via an email with a crafted attachment, potentially leading to root command execution. Only gateways with the File Reputation service enabled and a Content Scanner Tools package older than 25.3.0.5525 are vulnerable. Fixes have shipped since Sept 14 in AsyncOS 15.5.5-014 and 16.5.0-780, and as a Content Scanner Tools update 25.3.0.5525+ that installs without a software upgrade or restart. Distinct from the earlier CVE-2026-76461.
