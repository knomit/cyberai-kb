---
type: observation
domain: [technology, ai, voice]
confidence: 0.8
sources: 2
evidence_weight: 0.6153846153846154
entities: [OpenAI, GPT-Live-1, GPT-Live-1 mini, GPT-5.5, ChatGPT Voice, Advanced Voice Mode, GPT-Realtime-2]
refs: ['kb://d88770a51516/kb/technology/ai/models/openai/gpt-live-voice/2602b6fd.md', 'kb://d88770a51516/kb/technology/ai/products/gpt-live/5a70df82.md']
---
# OpenAI's GPT-Live-1 voice models (July 8, 2026) replaced Advanced Voice Mode with a full-duplex architecture that delegates hard queries to GPT-5.5 while continuing to speak

THE RELEASE. On July 8, 2026, OpenAI released a pair of voice models — GPT-Live-1 and GPT-Live-1 mini — powering a rebuilt ChatGPT Voice that replaces Advanced Voice Mode (AVM). Both are speech-in/speech-out and process incoming and outgoing audio continuously (full-duplex) rather than in discrete turns.

THE DELEGATION MECHANISM. When a query needs deeper reasoning, web search, or multi-step tool use, the voice model delegates to GPT-5.5 and keeps talking while that model works, weaving the result back in. GPT-Live-1 offers user-selectable reasoning effort (Instant/Medium/High); Instant runs GPT-5.5 Instant, Medium/High run GPT-5.5 Thinking. GPT-Live-1 mini only calls GPT-5.5 Instant.

THE ARCHITECTURE. Per OpenAI's engineering write-up (surfaced via TLDR AI, Aug 4, 2026), the voice stack was rebuilt around a full-duplex model that listens and speaks simultaneously, combining four elements to keep conversations responsive while supporting advanced reasoning: stateful inference, asynchronous delegation, dynamic context management, and low-latency media transport.

PACKAGING AND AVAILABILITY. It ships with 9 predefined remastered voices and safeguards blocking mimicry of real voices. Available on iOS, Android, and ChatGPT.com globally; GPT-Live-1 is default for Go/Plus/Pro, mini for the free plan. No developer API shipped at release — the developer voice option remains GPT-Realtime-2. OpenAI says more than 150 million people use ChatGPT voice/dictation weekly.

WHAT THIS DOES NOT MEAN: the usage figure and the architecture description are OpenAI's own, not independently verified. This fact records the release and its stated design; comparative benchmark results against AVM are recorded separately, and those comparisons were run against OpenAI's own predecessor rather than rival voice models.
