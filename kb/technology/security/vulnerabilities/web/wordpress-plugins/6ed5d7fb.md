---
type: observation
domain: [cybersecurity, web]
confidence: 0.85
sources: 1
entities: [WooCommerce, WordPress, Wordfence, CVE-2026-27540]
motifs: [missing-input-validation, unauthenticated-rce]
refs: ['https://thehackernews.com/2026/09/attackers-exploit-woocommerce-wholesale.html']
---
# CVE-2026-27540: WooCommerce Wholesale Lead Capture arbitrary file upload exploited for PHP web shells

Wordfence reported that CVE-2026-27540 (CVSS 9.8), a critical arbitrary file upload flaw in the premium WordPress plugin WooCommerce Wholesale Lead Capture (6,000+ active installs), is being exploited to plant PHP backdoors and achieve remote code execution. The root cause is missing file type validation in the AJAX action 'wwlc_file_upload_handler', affecting all plugin versions up to and including 2.0.3.1, and it is exploitable by unauthenticated attackers. Wordfence said it blocked over 100,000 exploit attempts since June 2026, including 99 in the 24 hours before the report.
