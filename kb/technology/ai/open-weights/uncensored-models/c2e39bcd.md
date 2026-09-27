---
type: observation
domain: [ai-safety, open-weights, measurement]
confidence: 0.75
sources: 1
entities: [10a Labs, HuggingFace, Qwen, Llama, Gemma, Mistral, Phi, Ollama]
motifs: [redistribution-as-persistence, producer-distributor-split]
refs: ['https://arxiv.org/abs/2609.05241']
---
# 3,471 uncensored model repos on HuggingFace, with redistribution rather than production as the persistence layer

Startup 10a Labs mapped the uncensored open-weight model ecosystem and found 3,471 uncensored model repositories hosted on HuggingFace. 'Uncensoring' means techniques that intentionally strip the safety guardrails present when open-weight models are released — activation-space abliteration (suppressing refusal directions), malicious fine-tuning, and model merging among them.

Key measurements: the top five modified model families are Qwen, Llama, Gemma, Mistral/Mixtral, and Phi. The top three uncensored model types are uncensored chatbots, cybersecurity tools, and document processing tools. Each original uncensored model is repackaged an average of 2.4 times. Producers and redistributors barely overlap — 1,055 producers and 1,011 redistributors, with only 24% of producers also redistributing. Ten actors account for 45% of all non-dataset HuggingFace repositories in the set. GitHub application creation rose from 30 per month in mid-2024 to 140–188 per month by late 2025, tracking the maturation of the Ollama distribution layer. Chinese-origin models are 38% of all identified uncensored repositories, and the Chinese share of NEW uncensored production rose from 1% in Q1 2024 to 55% in Q2 2025.

The paper's central claim is that REDISTRIBUTION, not production, is what makes uncensored models persist — so takedown strategies aimed at producers address the smaller and less durable half of the population.
