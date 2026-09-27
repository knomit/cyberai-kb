---
type: observation
domain: [cybersecurity, vulnerabilities, web-servers, dos]
confidence: 0.85
sources: 1
entities: [HTTP/2 Bomb, HPACK, NGINX, Apache HTTPD, Cloudflare Pingora, Envoy, Microsoft IIS]
motifs: [limit-measures-wrong-quantity]
refs: ['https://thehackernews.com/2026/06/new-http2-bomb-vulnerability-allows.html']
---
# HTTP/2 Bomb (HPACK + Slowloris): remote DoS on NGINX, Apache, IIS, Envoy, Cloudflare Pingora

Researcher 'Calif' discovered an HTTP/2 remote denial-of-service exploit, codenamed HTTP/2 Bomb, discovered using OpenAI Codex by chaining two known techniques: (1) HPACK compression bomb — HTTP/2's HPACK header compression allows one byte on the wire to expand into one full header allocation on the server, repeated thousands of times per request; (2) Slowloris-style hold — a zero-byte flow-control window that keeps the server from ever freeing any allocated memory. Combined, 'The classic bomb stuffs a large value into the table and references it repeatedly, so servers learned to cap the total decoded header size. Our variant goes the other way: the header is nearly empty, and the amplification comes from the per-entry bookkeeping the server allocates around it. The decoded-size limit never fires because there's almost nothing to decode.' Affected: NGINX, Apache HTTPD, Microsoft IIS, Envoy, and Cloudflare Pingora (default HTTP/2 configuration). Impact: a single client on a 100Mbps home connection can potentially render a vulnerable server inaccessible within seconds. Related historical CVEs: CVE-2016-6581 (HPACK Bomb), CVE-2025-53020 (Apache memory exhaustion), CVE-2016-8740, CVE-2016-1546.
