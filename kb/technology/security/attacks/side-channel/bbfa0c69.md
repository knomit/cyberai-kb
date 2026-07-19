---
type: observation
domain: [cybersecurity, side-channel, browser-security, privacy]
confidence: 0.95
sources: 1
entities: [FROST, OPFS, Graz University of Technology]
refs: ['https://thehackernews.com/2026/06/new-frost-side-channel-attack-lets.html', 'https://thehackernews.com/2026/06/new-frost-attack-lets-websites-track.html', kb/technology/security/privacy/side-channel-attacks/c2057459.md]
---
# FROST: JavaScript SSD timing side-channel fingerprints browser activity and app usage without user interaction

Researchers from Graz University of Technology and Liebherr-Transportation Systems GmbH disclosed FROST (Fingerprinting Remotely using OPFS-based SSD Timing), a side-channel attack from JavaScript that exploits the Origin Private File System (OPFS) API to leak sensitive information from the browser on both Linux and macOS. The attack measures tiny changes in SSD access times as a side channel, turning normal browser activity into a privacy leak. After tricking a victim into clicking a malicious link, an attacker can monitor the victim's activity on the host system — including website visits and application usage — without further user interaction. The attack also enables fingerprinting of specific applications, allowing inference of when apps were opened.
