---
type: synthesis
domain: [ai, voice, product-metrics]
confidence: 0.7
sources: 1
evidence_weight: 0.4736842105263158
origin: discovered
entities: [OpenAI, ChatGPT, GPT-Live-1, GPT-Live-1 mini, GPT-Realtime-2, WebRTC, ByteByteGo]
refs: ['kb://d88770a51516/kb/technology/ai/infrastructure/real-time/83488dd5.md', 'kb://d88770a51516/kb/technology/ai/models/openai/gpt-live-voice/2602b6fd.md', 'kb://d88770a51516/kb/technology/ai/models/audio/6f6c3013.md', 'kb://d88770a51516/kb/technology/ai/products/gpt-live/5a70df82.md', 'kb://d88770a51516/kb/technology/ai/products/voice/f5d644cd.md']
---
# OpenAI's voice user base is >150M weekly, not the ~900M figure a WebRTC infrastructure record's title implies — the larger number is the platform population the transport serves

Two user figures for OpenAI voice sit in this corpus and differ by roughly 6x. They are not both counts of voice users, and the larger one is the more citable because it is in a title.

THE TWO FIGURES.
- kb/technology/ai/infrastructure/real-time/83488dd5.md is titled 'OpenAI uses WebRTC to deliver low-latency voice AI to 900M users', describing an engineering analysis of how OpenAI runs its voice features 'for roughly 900 million users' at low latency.
- kb/technology/ai/models/openai/gpt-live-voice/2602b6fd.md records OPENAI'S OWN statement alongside the GPT-Live-1 release of 8 July 2026: 'more than 150 million people use ChatGPT voice/dictation WEEKLY.'

WHY THEY CANNOT BOTH COUNT VOICE USERS. If OpenAI states that more than 150 million people use voice or dictation weekly, ~900 million cannot simultaneously be the voice-using population — the vendor's own figure would then understate its adoption more than sixfold. The consistent reading is that ~900 million describes the PLATFORM POPULATION the WebRTC transport is provisioned across, not the subset that uses voice. This is corroborated by other records in this corpus putting ChatGPT's total user base at roughly 1 billion, a figure ~900 million approaches and >150 million does not.

WHY IT MATTERS. The overstated number is the one in a title, which is what a citation carries. 'OpenAI delivers voice AI to 900M users' reads as an adoption statistic and would be quoted as one. The record it titles carries CONFIDENCE 0.55 WITH ZERO RECORDED SOURCES, resting on a single engineering blog post, while the 150M figure comes from OpenAI directly in a record with two sources. The weaker-sourced number is the more quotable one.

SCOPE NOTE — THREE DIFFERENT VOICE POPULATIONS ARE IN PLAY and should not be merged: consumer ChatGPT Voice (GPT-Live-1 for Go/Plus/Pro, GPT-Live-1 mini as the free-plan default), the DEVELOPER surface (GPT-Realtime-2, which remained the developer voice option because GPT-Live shipped with no developer API), and the total platform population the transport layer serves. The 150M weekly figure covers voice/dictation use; nothing here breaks it down by tier or by consumer-versus-developer.

WHAT THIS DOES NOT MEAN:
- It does NOT claim the ByteByteGo analysis is wrong. Provisioning low-latency real-time audio across a ~900M-user platform is a coherent engineering claim and may be exactly what the source said; the defect is in how the record's TITLE reads, not necessarily in the underlying analysis.
- It does NOT establish the exact voice-user count. '>150 million weekly' is a floor, is vendor-stated, and is not independently verified.
- It does NOT claim the figures are contemporaneous in a way that permits arithmetic — the WebRTC record is dated 2 July 2026 and the GPT-Live release 8 July 2026, six days apart, but neither states a measurement window beyond 'weekly' for the smaller figure.
- Voice usage measured 'weekly' and a platform population measured however ByteByteGo measured it are different units; this record reconciles what each refers to, and does not compute a ratio between them.
