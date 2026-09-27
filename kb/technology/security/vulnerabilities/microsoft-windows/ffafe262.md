---
type: observation
domain: [cybersecurity, patch-management, vulnerability-management]
confidence: 0.9
sources: 3
evidence_weight: 0.7297297297297297
entities: [Microsoft, Windows, CVE-2026-85880, CVE-2026-81963, Patch Tuesday]
motifs: [patch-volume-growth, local-privilege-escalation, triage-overload]
refs: ['https://www.securityweek.com/microsoft-patches-record-974-vulnerabilities-including-two-exploited-zero-days/', 'https://thehackernews.com/2026/09/microsoft-patches-record-974-flaws.html']
---
# Microsoft's September 2026 Patch Tuesday set a record at 974 CVEs with two exploited Windows zero-days

Microsoft's September 2026 Patch Tuesday addressed 974 vulnerabilities (999 counting 25 non-Microsoft CVEs), a record and roughly a 70% increase over the prior record of 569 set in July 2026; the year's running total passed 2,600, already more than double the previous record year of 2020 (1,245), with three months remaining.

Product breakdown: 723 in Windows, 111 in Office, 62 in SQL, 22 in Developer Tools, with over 110 rated critical.

Two of the flaws were actively exploited in the wild, both local privilege escalations to SYSTEM: CVE-2026-85880, a heap buffer overflow in the Windows Advanced Local Procedure Call (ALPC) subsystem, and CVE-2026-81963, an improper link resolution before file access ('link following') defect in the Windows Update Stack.

The release also included high-impact remote code execution fixes for Windows DNS Server, Remote Desktop Services, DHCP Server, Windows Shell, Exchange Server, SharePoint, and SQL Server.
