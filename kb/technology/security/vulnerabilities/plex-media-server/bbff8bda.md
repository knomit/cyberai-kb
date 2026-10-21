---
type: observation
domain: [security, vulnerability]
confidence: 0.7
sources: 1
entities: [Plex Media Server, Plex2Shell, CVE-2026-96652, CVE-2026-96654]
motifs: [chained-low-severity-flaws]
refs: ['https://thehackernews.com/2026/10/hackers-exploit-plex2shell-flaws-to.html']
---
# Plex2Shell: chained Plex Media Server vulnerabilities exploited for miners and proxy backdoor

Threat actors began exploiting 'Plex2Shell', a chain of four Plex Media Server vulnerabilities (reported by researcher boredhackerblog), a day after a PoC was published, deploying cryptocurrency miners and reverse-proxy software. Chain includes CVE-2026-96652 (CVSS 5.3, unauthenticated SSRF via /player/timeline 'protocol' parameter) and CVE-2026-96654 (CVSS 6.9, URL neutralization flaw in 'searchOne'). Low individual CVSS scores understate the chained impact.
