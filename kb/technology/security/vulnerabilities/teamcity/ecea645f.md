---
type: observation
domain: []
confidence: 0.85
sources: 1
entities: [JetBrains, TeamCity, CVE-2026-63077]
motifs: [guard-misses-the-act]
refs: ['https://thehackernews.com/2026/07/critical-teamcity-flaw-could-let.html']
---
# TeamCity CVE-2026-63077 unauth RCE

JetBrains disclosed CVE-2026-63077 (CVSS 9.8), a critical flaw affecting all TeamCity On-Premises versions that lets an unauthenticated attacker with HTTP(S) access bypass authentication via the agent polling protocol and execute arbitrary OS commands with the TeamCity server process privileges. Fixed in versions 2025.11.7 and 2026.1.3; TeamCity Cloud was already patched. Reported by Antoni Tremblay on July 10, 2026.
