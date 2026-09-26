---
type: observation
domain: [security]
confidence: 0.85
sources: 1
entities: [Roundcube, CVE-2026-48842, Canadian Centre for Cyber Security, SentinelOne]
refs: ['https://thehackernews.com/2026/09/roundcube-pre-auth-sql-injection-flaw.html']
---
# CVE-2026-48842: unauthenticated SQL injection in Roundcube Webmail actively exploited

CVE-2026-48842 (CVSS 8.1) is a pre-authentication SQL injection vulnerability in the virtuser_query plugin of Roundcube Webmail (versions 1.6.x before 1.6.16 and 1.7.x before 1.7.1), caused by a preg_replace() backslash-escape bypass that lets unauthenticated attackers inject arbitrary SQL into Roundcube's database backend, potentially exposing mail account credentials and stored messages (per SentinelOne). The Canadian Centre for Cyber Security has warned it is being actively exploited in the wild, even though Roundcube released patches (1.6.16) in May 2026.
