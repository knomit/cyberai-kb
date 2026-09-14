---
type: observation
domain: [ai-security, intellectual-property, cybersecurity]
confidence: 0.78
sources: 2
entities: [Anthropic, Claude, Alibaba, Moonshot, DeepSeek, Z.ai, MiniMax, GTG-16005]
motifs: [model-capability-extraction, fake-account-farming, upstream-request-rerouting]
refs: ['https://thehackernews.com/2026/09/anthropic-says-seven-china-based-ai.html', 'https://www.cnbc.com/2026/09/11/chinese-ai-labs-moonshot-deepseek-alibaba-anthropic.html']
---
# Anthropic says seven China-based AI labs ran industrial-scale illicit distillation against Claude

Anthropic said on September 10-11, 2026 that it identified and disrupted industrial-scale illicit distillation attacks against Claude originating from seven China-based labs, naming Alibaba, Moonshot, DeepSeek, Z.ai (formerly Zhipu) and MiniMax among them. Illicit distillation here means covertly extracting a model's capabilities and replicating them in another model without authorization, typically through networks of fraudulent accounts created with stolen credit cards, login credentials and API keys, plus proxy networks. The largest campaign Anthropic detected, GTG-16005, involved Alibaba-affiliated operators and comprised 151 million observed exchanges between May and July 2026, peaking around 3 million exchanges per day from more than 3,500 fraudulent accounts, concentrated on agentic tasks, software engineering, kernel development and long-horizon tasks. Anthropic also said that in some cases unauthorized labs rerouted their own users' requests to Claude, without those users' knowledge or permission, in order to harvest the resulting exchanges for training. These are Anthropic's attribution claims; the named companies' responses are not captured here.
