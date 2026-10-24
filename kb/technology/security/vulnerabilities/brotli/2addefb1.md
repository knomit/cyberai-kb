---
type: observation
domain: [security, vulnerability, vulnerabilities]
confidence: 0.8
sources: 1
entities: [Brotli, Google, Node.js, Bun, Envoy, Imperva, CVE-2026-111497]
motifs: [vendored-dependency-lag]
refs: ['https://thehackernews.com/2026/10/brotli-decoder-flaw-behind-nodejs-rce.html']
---
# Brotli decoder memory-corruption flaw CVE-2026-111497 affects Node.js, Bun, Python Brotli, Envoy

A memory-corruption flaw in Google's Brotli decoder (CVE-2026-111497) lets crafted compressed data overwrite past the end of a buffer, potentially causing a crash, memory leak or attacker-controlled code execution. Affected programs include Bun, the Python Brotli and brotlicffi packages, and Envoy proxies configured to decompress Brotli. Imperva researchers demonstrated code execution on one unpatched Node.js build only; it has not been shown on the other software and no real-world attacks were reported. Disclosed October 21, 2026 when Node.js and Google shipped fixes. Because each program bundles its own copy of the decoder, each must update independently. Does NOT mean exploitation is confirmed for Bun, Python or Envoy.
