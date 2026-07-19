---
type: observation
domain: [cybersecurity, supply-chain]
confidence: 0.8
sources: 1
origin: discovered
entities: [npm, Vite, ViteVenom, ChainVeil, Checkmarx, SuccessKey]
refs: ['https://thehackernews.com/2026/07/seven-malicious-vite-npm-packages-use.html']
---
# ViteVenom: 7 malicious npm packages use four-tier blockchain C2 to deliver a RAT

Checkmarx disclosed a software supply chain campaign, codenamed 'ViteVenom', involving seven malicious npm packages targeting the Vite frontend tooling ecosystem. It is an expansion of the earlier 'ChainVeil' activity, which used an unprecedented four-tier blockchain-based command-and-control infrastructure spanning Tron, Aptos, and Binance Smart Chain to deliver a remote access trojan capable of reverse shell, credential harvesting, file exfiltration, and persistent backdoor injection. Distributing C2 across blockchains makes the infrastructure very hard to take down. Checkmarx (researcher Pavan Gudimalla) attributed it to a threat actor named 'SuccessKey', with evidence of activity as far back as February 27.
