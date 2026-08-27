---
type: observation
domain: [security, vulnerability, linux, cybersecurity, privilege-escalation]
confidence: 0.85
sources: 0
entities: [DirtyClone, CVE-2026-43503, Dirty Frag, JFrog, Linux kernel, DirtyFrag, JFrog Security Research]
refs: ['https://thehackernews.com/2026/06/new-dirtyclone-linux-kernel-flaw-lets.html']
---
# DirtyClone (CVE-2026-43503) Linux kernel flaw enables local root

Researchers (JFrog) detailed DirtyClone (CVE-2026-43503), a new variant of the Dirty Frag Linux kernel flaw that lets local users gain root privileges via cloned packets. It works on Debian, Ubuntu, and Fedora with default namespace configurations and requires the CAP_NET_ADMIN capability, frequently obtainable via unprivileged user namespaces. It poses the highest risk to multi-tenant cloud environments.
