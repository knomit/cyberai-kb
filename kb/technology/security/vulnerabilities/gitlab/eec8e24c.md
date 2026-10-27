---
type: observation
domain: [security, rce]
confidence: 0.8
sources: 1
entities: [GitLab, Ruby, Onigmo]
refs: ['https://thehackernews.com/2026/10/critical-gitlab-flaw-cvss-100-could.html', 'https://docs.gitlab.com/releases/patches/patch-release-gitlab-19-5-1-released/']
---
# GitLab CVE-2026-110264 (CVSS 10.0): unauthenticated RCE via regex integer overflow in Ruby Onigmo

GitLab patched CVE-2026-110264 (CVSS 10.0), an unauthenticated code-execution flaw from an integer overflow compiling a crafted regular expression. Fixed in GitLab CE/EE 19.5.1, 19.4.3, 19.3.6, 19.2.9, 19.1.9, 19.0.10 and 18.11.13. Ruby released 4.0.9, 3.4.12 and 3.3.13 fixing the underlying Onigmo regex bugs (CVE-2026-89078, -93577, -97229, -110264).
