---
type: synthesis
domain: [security, zero-day, network-security]
confidence: 0.85
sources: 2
evidence_weight: 0.6226415094339622
entities: [SonicWall, UTA0533, Secure Mobile Access 1000, CISA, CVE-2026-15409, CVE-2026-15410]
refs: ['https://thehackernews.com/2026/07/sonicwall-sma-zero-days-exploited.html', 'https://thehackernews.com/2026/07/two-sonicwall-sma-1000-zero-days.html', 'https://psirt.global.sonicwall.com/vuln-detail/SNWLID-2026-0008', 'https://www.cisa.gov/news-events/alerts/2026/07/14/cisa-adds-four-known-exploited-vulnerabilities-catalog']
---
# SonicWall SMA 1000 zero-days (CVE-2026-15409 / CVE-2026-15410) exploited by UTA0533 for root access

SonicWall warned in July 2026 of active exploitation of two zero-day vulnerabilities in its Secure Mobile Access (SMA) 1000 series appliances. A previously undocumented threat actor codenamed UTA0533 has been attributed to the exploitation, which began before public disclosure since June 22, 2026, and was uncovered during an incident-response investigation; the impacted organization was not identified. The actor gained root access.

The two flaws: CVE-2026-15409 (CVSS 10.0) is a server-side request forgery (SSRF) flaw a remote unauthenticated attacker can exploit to make the appliance issue requests to an unintended location. CVE-2026-15410 (CVSS 7.2) is a post-authentication code-injection flaw in the Appliance Management Console (AMC) allowing a remote authenticated attacker to execute arbitrary OS commands as administrator under certain conditions. SonicWall said it 'investigated multiple cases indicating the active exploitation of the vulnerabilities.'

Fixes ship in versions 12.4.3-03453 (platform-hotfix) and higher, and 12.5.0-02835 (platform-hotfix) and higher. Indicators of compromise include requests to /__api__/login or /__api__/logout returning HTTP 200 in extraweb_access.log, /wsproxy requests with suspicious host parameters returning HTTP 101, hotfix rollbacks with path-traversal names in ctrl-service.log, and routes for /__api__/login or /__api__/logout in /var/lib/unit/conf.json (URIs that do not exist in legitimate configuration). If found, SonicWall advises re-imaging physical appliances or redeploying virtual ones, rotating all user and administrator passwords, and resetting TOTP tokens. CISA added the flaws to its KEV catalog.
