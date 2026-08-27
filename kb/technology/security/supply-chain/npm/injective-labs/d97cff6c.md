---
type: observation
domain: [cybersecurity, supply-chain]
confidence: 0.85
sources: 0
entities: [Injective Labs, npm, GitHub, '@injectivelabs/sdk-ts', cryptocurrency wallet]
motifs: [reputation-survives-replacement]
refs: ['https://thehackernews.com/2026/07/injective-labs-github-compromise-pushes.html']
---
# Injective Labs GitHub compromise pushed wallet-key-stealing npm package

Threat actors compromised the Injective Labs SDK GitHub repository and published a malicious npm package, @injectivelabs/sdk-ts@1.20.21, released July 8, 2026. It contained fake telemetry functionality that exfiltrated cryptocurrency wallet private keys and mnemonic seed phrases. The malicious code was introduced via commits from a GitHub account with an established contribution history to the repo. The version was later deprecated on npm, though compromised release artifacts remained downloadable from GitHub.
