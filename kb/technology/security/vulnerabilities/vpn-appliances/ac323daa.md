---
type: observation
domain: [security, threat-intel]
confidence: 0.85
sources: 1
entities: [SonicWall, SMA 1000, UTA0533, KNUCKLEBALL, Volexity, CVE-2026-15409, CVE-2026-15410]
motifs: [repeat-vendor-exposure, chained-preauth-postauth]
refs: ['https://thehackernews.com/2026/09/attackers-exploit-two-sonicwall-sma.html', 'https://thehackernews.com/2026/07/sonicwall-sma-zero-days-exploited.html']
---
# These are the second pair of exploited SonicWall SMA 1000 zero-days in about two months

The September 2026 SMA 1000 flaws (CVE-2026-83548/83549) came roughly a month after SonicWall shipped fixes in July 2026 for two other SMA 1000 flaws, CVE-2026-15409 (CVSS 10.0) and CVE-2026-15410 (CVSS 7.2), which a threat actor tracked by Volexity as UTA0533 exploited to deploy KNUCKLEBALL malware. Both incidents follow the same shape: a pre-auth flaw chained with a privileged command-execution flaw on the same appliance.
