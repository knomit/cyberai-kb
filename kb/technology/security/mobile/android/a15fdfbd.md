---
type: observation
domain: [security, mobile]
confidence: 0.85
sources: 1
entities: [Google, Android 17, Advanced Protection, AccessibilityService]
refs: ['https://thehackernews.com/2026/10/android-17-advanced-protection-locks.html']
---
# Android 17 Advanced Protection restricts AccessibilityService to verified Accessibility Tools

In Android 17, enabling Advanced Protection automatically restricts AccessibilityService API access to verified apps categorized as Accessibility Tools. Google announced it on 2026-10-01 to close a major malware/financial-fraud pathway, since malicious apps commonly abuse the API. It applies only when Advanced Protection is enabled, not to all devices by default.
