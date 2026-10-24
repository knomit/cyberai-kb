---
type: observation
domain: [security, vulnerabilities]
confidence: 0.8
sources: 1
entities: [Brotli, CVE-2026-111497, Node.js, Bun, Imperva, Envoy, Google]
motifs: [vendored-dependency-lag]
refs: ['https://thehackernews.com/2026/10/brotli-decoder-flaw-behind-nodejs-rce.html']
---
# Brotli decoder memory-corruption flaw CVE-2026-111497 affects Node.js, Bun, Python Brotli, Envoy

CVE-2026-111497 is a memory-corruption (out-of-bounds write) flaw in Google's Brotli decoder; crafted compressed data can overwrite past the end of a buffer, causing a crash, memory leak or attacker-controlled code execution. Imperva researchers demonstrated code execution only on one unpatched Node.js build; the same has not been demonstrated on Bun, the Python Brotli and brotlicffi packages, or Envoy proxies configured to decompress Brotli, and no real-world attacks were reported. Disclosed October 21, 2026 with fixes from Node.js and Google. Because each program ships its own copy of the decoder, each must update its copy separately; patching Google's library alone does not protect other products. Reported by The Hacker News on 2026-10-24.
