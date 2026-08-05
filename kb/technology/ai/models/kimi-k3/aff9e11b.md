---
type: observation
domain: []
confidence: 0.8
sources: 2
entities: [Kimi K3, Moonshot, Mixture of Experts, vLLM, Moonshot AI]
refs: ['https://sebastianraschka.com/blog/2026/kimi-k3-architecture-notes.html', 'https://x.com/vllm_project/status/2081788542079123939', 'https://threadreaderapp.com/thread/2081760186235289764.html', kb/technology/ai/models/kimi-k3/aff9e11b.md]
---
# Kimi K3: 2.8-trillion-parameter multimodal MoE with 1M-token context

Kimi K3 (Moonshot) is a 2.8-trillion-parameter multimodal mixture-of-experts model with 16 of 896 experts active per token and a context window of up to 1 million tokens. Its architecture is described as a scaled-up production version of the earlier Kimi Linear model, trending toward better inference efficiency and adding native multimodal support. Analyses of its architecture and vLLM serving were published by Sebastian Raschka and the vLLM project.
