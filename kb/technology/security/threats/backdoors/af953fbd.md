---
type: observation
domain: [security, malware]
confidence: 0.8
sources: 0
entities: [Mistic, MLTBackdoor, KongTuke, ModeloRAT, Symantec, Carbon Black]
refs: ['https://thehackernews.com/2026/06/new-mistic-backdoor-linked-to-kongtuke.html']
---
# Mistic backdoor linked to KongTuke, deployed with ModeloRAT

Symantec and Carbon Black's Threat Hunter Team reported a new stealthy backdoor named Mistic (aka MLTBackdoor) used in suspected financially motivated attacks on insurance, education, IT, and professional-services organizations since April 2026. It is linked to initial access broker KongTuke (aka 404 TDS, Chaya_002, LandUpdate808, TAG-124, Woodgnat) and dropped alongside ModeloRAT, a Python RAT first flagged by Huntress in January 2026. The backdoor runs payloads in memory with no file written to disk and includes a self-delete kill switch, consistent with long-term, low-visibility access.
