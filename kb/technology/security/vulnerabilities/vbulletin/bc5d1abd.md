---
type: observation
domain: []
confidence: 0.8
sources: 1
entities: [vBulletin, CVE-2026-61511, SSD Secure Disclosure]
refs: ['https://thehackernews.com/2026/07/public-exploit-released-for-patched.html']
---
# Public exploit for vBulletin CVE-2026-61511

On July 27, 2026, SSD Secure Disclosure released a public exploit for vBulletin CVE-2026-61511, showing how an unauthenticated request can reach PHP's eval() function and execute code with no account or interaction required. Affected: vBulletin 6.2.1 and earlier, and 6.1.6 and earlier. vBulletin patched 6.2.1, 6.2.0 and 6.1.6 in late June and released fixed version 6.2.2 on July 1, ~4 weeks before the exploit went public. As of July 27, no in-the-wild exploitation was confirmed and the CVE was not in CISA's KEV catalog.
