---
type: observation
domain: [security, vulnerabilities]
confidence: 0.85
sources: 1
entities: [TeamViewer, CVE-2026-111585]
refs: ['https://thehackernews.com/2026/10/teamviewer-flaw-lets-remote-computers.html']
---
# TeamViewer CVE-2026-111585: malicious host can attack the viewer; fixed in 15.83

TeamViewer fixed CVE-2026-111585 (CVSS 8.8): a malicious or compromised host in a remote session can crash the viewer's TeamViewer and, depending on platform, run code on the viewer's computer, only after the user starts a remote-control session to that host. Affects Full Client (Windows, Linux, macOS), Windows Portable and Android Remote Control app in all versions before 15.83; fixed in 15.83. The bulletin lists Full Client, Portable and Android app, not the Host.
