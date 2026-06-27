---
type: observation
domain: [security, vulnerability]
confidence: 0.8
sources: 0
entities: [Squid, Squidbleed, CVE-2026-47729, Calif.io]
refs: ['https://thehackernews.com/2026/06/29-year-old-squid-proxy-bug-squidbleed.html']
---
# Squidbleed (CVE-2026-47729) leaks cleartext HTTP via Squid proxy

Researchers at Calif.io disclosed a heap over-read in the Squid web proxy in June 2026, named 'Squidbleed' (CVE-2026-47729) after Heartbleed. The bug traces to a 1997 FTP-parsing change and is live in Squid's default configuration. It lets a trusted client already permitted to use the proxy (e.g., on shared school/office/public Wi-Fi networks) leak another user's cleartext HTTP request, including credentials or session tokens. Only traffic Squid can read is exposed — normal HTTPS in an opaque CONNECT tunnel is safe, but cleartext HTTP and TLS-terminating/inspecting setups are affected.
