---
type: observation
domain: [cybersecurity, vulnerability, privilege-escalation]
confidence: 0.85
sources: 0
entities: [CVE-2026-43503, DirtyClone, DirtyFrag, Linux kernel, JFrog Security Research]
refs: ['https://thehackernews.com/2026/06/new-dirtyclone-linux-kernel-flaw-lets.html']
---
# CVE-2026-43503 'DirtyClone': Linux kernel root escalation via cloned network packets

DirtyClone (CVE-2026-43503, CVSS 8.8) is a Linux kernel privilege escalation in the 'DirtyFrag' family. JFrog Security Research published a working exploit walkthrough on June 25, 2026 — the first public demonstration for this variant. When the kernel internally copies a network packet, two helper functions drop a safety flag marking the packet memory as shared with an on-disk file; that missing flag is the vulnerability. An attacker loads a privileged binary (e.g. /usr/bin/su) into memory, wires those pages into a network packet, forces the kernel to clone it through an attacker-controlled IPsec tunnel, and the decryption step overwrites the binary's login checks to grant root. The fix landed in mainline Linux on May 21, 2026.
