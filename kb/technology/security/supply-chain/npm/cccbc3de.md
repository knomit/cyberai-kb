---
type: observation
domain: [security, supply-chain, software-development]
confidence: 0.85
sources: 0
entities: [GitHub, npm, npm v12]
refs: ['https://thehackernews.com/2026/06/github-to-disable-npm-install-scripts.html']
---
# GitHub to disable npm install scripts by default in npm v12

GitHub announced 'breaking changes' in npm version 12 (scheduled for release ~July 2026) that turn off install scripts by default to combat software supply chain attacks. GitHub called install-time lifecycle scripts the 'single largest code-execution surface in the npm ecosystem,' since 'npm install' runs scripts from every transitive dependency, letting a single compromised package run arbitrary code on developer machines or CI runners. The change requires explicit user approval to run such scripts.
