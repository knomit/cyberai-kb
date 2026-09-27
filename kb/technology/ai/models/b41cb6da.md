---
type: synthesis
domain: [AI models, AI safety, AI research, alignment]
confidence: 0.75
sources: 1
evidence_weight: 0.7361477572559367
origin: distilled
entities: [OpenAI, GPT-5.5, Codex, Anthropic, Claude Mythos, MIT, Nvidia]
refs: [kb/technology/ai/models/openai/76076e0a.md, kb/technology/ai/models/e35cd1be.md, kb/technology/ai/research/theory/027ccc6f.md, kb/technology/ai/research/theory/f64b961e.md, kb/technology/ai/infrastructure/compute/aa4e1d4b.md]
---
# Recursive self-improvement enters production: seven-week model cycles and the evaluation-velocity inversion

OpenAI released GPT-5.5 on April 24, 2026 — just seven weeks after GPT-5.4 — explicitly built using itself and Codex (recursive self-improvement / RSI). This marks a qualitative shift: RSI has moved from a research concept to a production mechanism. The seven-week release cycle is not a one-time sprint; it reflects an architectural decision to close the RSI loop in the build process itself, where the model being improved is also the primary tool used to improve it.

Three concurrent signals confirm this is a threshold crossing, not an isolated event: (1) Anthropic warned government officials and gave limited early access to Claude Mythos citing 'unprecedented cybersecurity risks' before release — the first instance of a frontier lab proactively preparing defensive infrastructure before a model ships, implying internal assessment that capabilities are outpacing external governance; (2) MIT's Recursive Language Models (RLMs) demonstrated that spawning submodels to process 11M+ tokens coherently is achievable with current infrastructure; (3) Nvidia's articulation of 'agentic scaling' as a fourth scaling law — AI talking to AI running hundreds of times — provides the theoretical framing for why RSI is becoming a structural driver rather than an optimization trick.

The decisive implication is the evaluation-velocity inversion: at seven-week release cycles driven by RSI, safety evaluation timelines (which typically require months for red-teaming, government briefing, and third-party audit) are structurally incompatible with the development pace. Anthropic's Mythos limited release and government briefing process is a partial compensatory mechanism, but it cannot scale to match RSI velocity without institutional change. The AI compute crisis (2500x token demand spike in five months) is partly a consequence of RSI loops consuming compute recursively — acceleration and infrastructure strain are the same phenomenon.
