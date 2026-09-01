---
type: concept
domain: [security, post-exploitation, browsers, malware]
confidence: 0.8
sources: 2
evidence_weight: 0.6226415094339622
entities: [SpecterOps, Chrome DevTools Protocol, App-Bound Encryption, Amnesia Stealer, Jamf, ClickFix]
motifs: [guard-misses-the-act]
refs: ['https://thehackernews.com/2026/08/chrome-devtools-technique-enables.html', 'kb://d88770a51516/kb/technology/security/malware/infostealers/fa3d82e9.md', 'kb://d88770a51516/kb/technology/security/techniques/browser-session-theft/aceb2a13.md', 'kb://d88770a51516/kb/technology/security/patterns/a63d0ff1.md']
---
# Enabling CDP in a live Chromium process sidesteps cookie replay protections

SpecterOps detailed a post-exploitation technique enabling the Chrome DevTools Protocol inside a live Google Chrome or Microsoft Edge process on Windows, given existing code execution on the host, to steal cookies, saved data and authenticated browser sessions. SpecterOps notes that App-Bound Encryption and device-bound session cookies make stealing and replaying session material harder but do not remove the value of an authenticated browser — once CDP is enabled, an operator uses the browser's own context to bypass replay protections, suggesting the next evolution of cookie theft may not require stealing the cookie database or ABE key at all.
