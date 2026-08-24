---
type: observation
domain: [security, vulnerability-management, networking]
confidence: 0.9
sources: 1
entities: [Cisco, Cisco Crosswork, Cisco Secure Workload]
refs: ['https://thehackernews.com/2026/08/cisco-patches-nine-crosswork-and-secure.html']
---
# Cisco patched nine Crosswork and Secure Workload flaws in August 2026, five rated CVSS 10.0

On 2026-08-20/21 Cisco published security updates covering nine vulnerabilities found during a continued comprehensive internal security review of its Crosswork platforms and Secure Workload Software.

Four flaws affect Crosswork Data Gateway, Crosswork Network Controller, and Crosswork Planning regardless of device configuration:
- CVE-2026-20030 (CVSS 10.0) — SQL injection
- CVE-2026-20357 (CVSS 10.0) — missing authentication for critical function
- CVE-2026-20358 (CVSS 10.0) — external control of file system
- CVE-2026-20359 (CVSS 9.9) — insufficiently protected credentials

These affect Cisco Crosswork release 7.2.1 and earlier and are fixed in 7.2.1-SP.

Five further flaws affect Cisco Secure Workload (both SaaS and on-premises):
- CVE-2026-20231 (CVSS 9.9) — improper neutralization of special elements (command/OS/argument injection)
- CVE-2026-20315 (CVSS 10.0) — improper access control (authorization, authentication, privileges, bypasses)
- CVE-2026-20317 (CVSS 10.0) — improper authentication (missing auth, auth bypass, reliance on untrusted inputs)
- CVE-2026-20318 (CVSS 9.6) — improper input validation (path traversal, external path control)
- CVE-2026-20319 (CVSS 7.5) — improper restriction of operations within memory buffer bounds (buffer overflow, OOB write)
