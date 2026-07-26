---
type: observation
domain: [cybersecurity, cryptography]
confidence: 0.8
sources: 2
evidence_weight: 0.6
entities: [OpenSSL, HollowByte, Okta, TLS]
refs: [kb/technology/security/vulnerabilities/openssl/1fbeb3cb.md, kb/technology/security/vulnerabilities/openssl/4f0e412e.md]
---
# OpenSSL 'HollowByte' DoS: 11-byte TLS request freezes server memory

Okta's Red Team disclosed a denial-of-service flaw in OpenSSL named 'HollowByte' (reported in The Hacker News weekly recap 2026-07-20). An 11-byte TLS handshake request causes an unpatched OpenSSL server to reserve up to 131 KB of memory for a message body that never arrives; the root cause is that OpenSSL trusts the 3-byte length field in the 4-byte handshake header. On glibc systems Okta tested, that memory is not reclaimed until the process restarts. OpenSSL shipped the fix on June 9, 2026 with no CVE, no advisory, and no changelog entry; fixed releases are OpenSSL 4.0.1, 3.6.3, 3.5.7, 3.4.6, and 3.0.21. Okta published the details in July 2026.
