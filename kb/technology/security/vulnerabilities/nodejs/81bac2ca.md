---
type: observation
domain: [security, vulnerabilities]
confidence: 0.85
sources: 1
entities: [Node.js, Imperva, Node2Shell, CVE-2026-111497, Brotli]
refs: ['https://thehackernews.com/2026/10/researchers-demonstrate-node2shell-rce.html']
---
# Imperva Node2Shell: RCE on official Node.js 24.22.0 via crafted Brotli data (CVE-2026-111497)

Imperva demonstrated code execution on the official Node.js 24.22.0 Linux arm64 image by feeding crafted data to the bundled Brotli decoder (CVE-2026-111497), without debugger or custom build. Node.js disclosed and fixed it Oct 21; fixed release 24.22.1 rejected the data. Exploit succeeded only after several tries and only on that build; other architectures and 22.x/26.x lines were not tested. Applications decoding untrusted Brotli data should update.
