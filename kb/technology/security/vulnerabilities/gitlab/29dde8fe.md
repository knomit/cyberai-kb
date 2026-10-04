---
type: reference
domain: [security, ai]
confidence: 0.85
sources: 1
entities: [GitLab, GitLab AI Gateway, Duo Agent Platform, CVE-2026-90970]
refs: ['https://thehackernews.com/2026/10/gitlab-patches-critical-self-hosted-ai.html']
---
# GitLab AI Gateway critical flaw CVE-2026-90970 (CVSS 9.9)

GitLab disclosed on 2026-10-02 a critical flaw, CVE-2026-90970 (CVSS 9.9), in its AI Gateway, which could let a logged-in user with Duo Agent Platform access run commands on the gateway under certain conditions. Fixed in gateway versions 19.2.4, 19.3.2 and 19.4.1. Only self-managed customers who host their own gateway must act (update immediately); GitLab.com, GitLab Dedicated and self-managed instances using a GitLab-hosted gateway are already fixed. Does NOT mean all GitLab instances are exposed.
