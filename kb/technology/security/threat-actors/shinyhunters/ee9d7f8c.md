---
type: observation
domain: [security]
confidence: 0.85
sources: 0
entities: [ShinyHunters, UNC6240, Oracle PeopleSoft, CVE-2026-35273, CISA, Google Mandiant]
refs: ['https://thehackernews.com/2026/06/shinyhunters-exploits-oracle-peoplesoft.html']
---
# ShinyHunters exploit Oracle PeopleSoft zero-day CVE-2026-35273

The ShinyHunters extortion crew (aka UNC6240) exploited an unpatched Oracle PeopleSoft flaw, CVE-2026-35273 (CVSS 9.8), a missing-authentication issue allowing unauthenticated takeover of PeopleSoft Enterprise PeopleTools. Google Mandiant observed exploitation between May 27 and June 9, 2026, with reconnaissance via MeshCentral, lateral movement, and data exfiltration (targeting PSEMHUB endpoints). The campaign mainly hit higher education (68% of 100+ notified orgs were universities/colleges). CISA added the flaw to its KEV catalog with a June 15, 2026 remediation deadline for federal agencies; stolen data was posted to the ShinyHunters leak site on June 9, 2026.
