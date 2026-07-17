---
type: observation
domain: [security, vulnerability, authentication]
confidence: 0.85
sources: 1
origin: distilled
entities: [n8n, CVE-2026-59208, Strix, RFC 8693]
refs: ['https://thehackernews.com/2026/07/n8n-token-exchange-flaw-could-let.html']
---
# CVE-2026-59208: n8n token-exchange flaw allowed cross-issuer account takeover

n8n Enterprise instances configured to trust more than one external token issuer matched an incoming JWT to a local user on the 'sub' claim alone, ignoring 'iss'. A valid token from issuer A carrying a sub belonging to a user under issuer B would log the attacker in as that user, with no password needed. Tracked as CVE-2026-59208; n8n shipped the fix on 24 June 2026 and the CVE record went public 9 July 2026. Token exchange is n8n's Enterprise route for OEM partners embedding the product, an RFC 8693 implementation. n8n credits the report to GitHub account 'bearsyankees', whose profile lists Strix, an AI penetration-testing agent vendor.
