---
type: observation
domain: [cybersecurity, web]
confidence: 0.8
sources: 1
origin: discovered
entities: [WordPress, CVE-2026-63030, CVE-2026-60137, wp2shell, Assetnote]
refs: ['https://thehackernews.com/2026/07/new-wp2shell-wordpress-core-flaw-lets.html']
---
# wp2shell: unauthenticated RCE in WordPress core (CVE-2026-63030 + CVE-2026-60137)

In July 2026, a WordPress core remote code execution chain dubbed 'wp2shell' was disclosed. It combines two bugs: CVE-2026-63030, a REST API batch-route confusion flaw, and CVE-2026-60137, a SQL injection in WordPress core. Chained, they let an anonymous, unauthenticated HTTP request execute code even on a bare install with zero plugins. All WordPress 6.9 and 7.0 sites were in range until WordPress shipped 6.9.5 and 7.0.2 and enabled forced auto-updates. The REST batch-route bug was found by Adam Kues at Assetnote (Searchlight Cyber's attack surface management arm). By July 18, 2026 the full mechanism had been published and a working proof-of-concept was public on GitHub.
