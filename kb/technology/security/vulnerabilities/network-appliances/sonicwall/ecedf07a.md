---
type: observation
domain: [security, zero-day, network-security]
confidence: 0.85
sources: 1
origin: discovered
entities: [SonicWall, CISA, Secure Mobile Access 1000]
refs: ['https://psirt.global.sonicwall.com/vuln-detail/SNWLID-2026-0008', 'https://www.cisa.gov/news-events/alerts/2026/07/14/cisa-adds-four-known-exploited-vulnerabilities-catalog', 'https://thehackernews.com/2026/07/two-sonicwall-sma-1000-zero-days.html']
---
# SonicWall SMA 1000 appliances hit by two actively exploited zero-days including a CVSS 10.0 SSRF

SonicWall warned in July 2026 of active exploitation of two zero-day vulnerabilities in its Secure Mobile Access (SMA) 1000 series appliances. CVE-2026-15409 (CVSS 10.0) is a server-side request forgery flaw a remote unauthenticated attacker can exploit to make the appliance issue requests to an unintended location. CVE-2026-15410 (CVSS 7.2) is a post-authentication code injection flaw in the Appliance Management Console (AMC) allowing a remote authenticated attacker to execute arbitrary OS commands as administrator under certain conditions. SonicWall said it 'investigated multiple cases indicating the active exploitation of the vulnerabilities.' Fixes ship in versions 12.4.3-03453 (platform-hotfix) and higher, and 12.5.0-02835 (platform-hotfix) and higher. Indicators of compromise include requests to /__api__/login or /__api__/logout returning HTTP 200 in extraweb_access.log, /wsproxy requests with suspicious host parameters returning HTTP 101, hotfix rollbacks with path-traversal names in ctrl-service.log, and routes for /__api__/login or /__api__/logout in /var/lib/unit/conf.json (URIs that do not exist in legitimate configuration). If found, SonicWall advises re-imaging physical appliances or redeploying virtual ones, rotating all user and administrator passwords, and resetting TOTP tokens. CISA added the flaws to its KEV catalog.
