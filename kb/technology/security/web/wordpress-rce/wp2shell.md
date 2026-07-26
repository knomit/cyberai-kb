---
type: observation
domain: [security, cybersecurity, web, wordpress]
confidence: 0.85
sources: 2
evidence_weight: 0.7101449275362319
entities: [WordPress, CVE-2026-63030, CVE-2026-60137, wp2shell, Searchlight Cyber, watchTowr, Assetnote, Jake Knott]
refs: [kb/technology/security/web/wordpress-rce/0499b496.md, kb/technology/security/vulnerabilities/wordpress/d9ac7fc6.md]
---
# WordPress 'wp2shell' (CVE-2026-63030 + CVE-2026-60137): pre-authenticated RCE in WordPress Core, actively exploited

'wp2shell' is a pre-authenticated remote code execution vulnerability in WordPress Core, formed by chaining CVE-2026-63030 and CVE-2026-60137. The flaws stem from WordPress core's REST batch API and can be exploited anonymously on a standard WordPress installation with no plugins or special conditions required, achieving full site compromise.

Disclosure/attribution: originally disclosed by Searchlight Cyber (with Assetnote); as of July 18, 2026 the flaws carry CVE IDs, the full mechanism has been published, and a working proof-of-concept is public. watchTowr principal researcher Jake Knott reported widespread impact across organizations of every size and vertical.

Exploitation: mass exploitation began in the early hours of a Saturday (UTC), initially using public exploit code to exfiltrate hashed credentials, with RCE following once further details became public.

Merged from two records reporting the same wp2shell vulnerability chain.
