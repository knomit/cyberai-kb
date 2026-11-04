---
type: observation
domain: [security, vulnerability, linux]
confidence: 0.75
sources: 1
entities: [CVE-2026-98432, Linux kernel, Red Hat, Ubuntu]
refs: ['https://thehackernews.com/2026/11/red-hat-patches-98-rated-linux-tcp-rce.html']
---
# CVE-2026-98432: Linux kernel IPv4 TCP use-after-free rated CVSS 9.8; Red Hat fixes 1 Nov, Ubuntu fixes in -proposed

CVE-2026-98432 is a remotely reachable, unauthenticated use-after-free in the Linux kernel IPv4 TCP code (present since Linux 4.4; IPv6 main path unaffected), rated CVSS 9.8 by the kernel CVE team (Red Hat initially rated it 5.9, Amazon Linux 8.1). Red Hat shipped fixed kernels 1 Nov 2026 for RHEL 8.10 (4.18.0-553.182.1.el8_10), 9.8 (5.14.0-687.64.1.el9_8), 10.2 (6.12.0-211.72.1.el10_2); reboot required. Ubuntu fixes for 22.04/24.04/26.04 LTS only in opt-in -proposed as of 2 Nov. Debian, Oracle, SUSE fixed in October. No in-the-wild exploitation reported and not in CISA KEV as of 30 Oct; PoC only triggers the race. Not a statement that it is unexploitable: Anthropic said an unreleased internal model produced a working remote root exploit in testing.
