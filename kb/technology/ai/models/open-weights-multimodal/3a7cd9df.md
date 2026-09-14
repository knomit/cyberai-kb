---
type: observation
domain: [open-weights-models, multimodal-models, ai-hardware]
confidence: 0.88
sources: 3
entities: [Z.ai, GLM-5.3-Flash, Ox Alpha, GLM-5.3, OpenRouter, OpenCode, Artificial Analysis, DeepSeek]
motifs: [anonymous-preview-launch, hardware-independence-signal]
refs: ['https://huggingface.co/zai-org/GLM-5.3-Flash', 'https://autoclaw.z.ai/blog/model/glm-5.3-flash/', 'https://www.deeplearning.ai/the-batch/issue-369']
---
# Z.ai's "Ox Alpha" revealed as GLM-5.3-Flash, an MIT-licensed multimodal MoE served on Chinese chips

Z.ai confirmed on 2026-08-26 that "Ox Alpha" — an anonymous model that had been free on the OpenCode harness and the OpenRouter marketplace for about a week, and became the most-used model on those services — was GLM-5.3-Flash, and released its weights under the permissive MIT license (zai-org/GLM-5.3-Flash on Hugging Face). Users had fingerprinted it to the GLM family within days from tokenizer outputs. Reported in The Batch 2026-09-04.

Specification: hybrid mixture-of-experts transformer, 320B total parameters, 18B active per token, 8 of 288 experts per token, ~45 layers; text, image and video in (up to 1,048,576 tokens), text out (up to 128,000 tokens). Reasoning is always on with low/high/max levels (max default); streaming, tool calling and context caching supported. API $0.15/$0.03/$0.50 per million input/cached/output tokens; GLM Coding Plan $18–$168 per month. Knowledge cutoff and pretraining data sources undisclosed.

What is architecturally new: this is the first GLM-5-family model whose vision capability was built in from pretraining rather than bolted onto a language model, pretrained from scratch on a 30-trillion-token multimodal corpus. It is also the first GLM model to mix linear attention (cost growing proportionally with input length, attending to nearby context) with sparse attention (attending to full context); Z.ai says the combination cuts attention compute to roughly a third of GLM-5.3's. An IndexPool step averages every four lookup vectors into one, and with the hybrid attention cuts the KV cache to under a quarter of GLM-5.3's (still above DeepSeek's and Kimi's best figures). It adopts Manifold-Constrained Hyper-Connections (mHC), a DeepSeek technique splitting layer-to-layer connections into parallel paths, for scaling efficiency. Training data was partly self-generated: the model rendered frontends, games and 3D scenes, observed the result and revised, and was trained on those attempts, with RL scoring on rendered page outcomes for front-end work.

Measured performance: 57 on Artificial Analysis' Intelligence Index at about $0.09 per task — close to open-weights leaders Kimi K3 and GLM-5.3 (both 60, at $0.84 and $0.68 per task), matching Claude Opus 4.8 at max reasoning ($2.03 per task) and beating Gemini 3.7 Flash (56, $0.40). Third on Artificial Analysis' GDPval-AA v2 at 1,765 Elo and best among open-weights models there. One-shot solved 63% of DeepSWE v1.1 at $0.24 per task, against GLM-5.3 at 69%/$3.99 and Claude Opus 5 (max reasoning) at 74%/$11.84; comparably sized DeepSeek V4 Flash solved 53% at twice the cost. The tradeoff is verbosity and speed: 150M tokens to complete the Intelligence Index against a 110M median, and ~45 tokens/second versus GLM-5.3's 78 and a 69 typical.

The notable claim, and the reason the story mattered: Z.ai says it served the entire free high-volume preview exclusively on domestic Chinese AI accelerators (reported as roughly 100,000 chips) — evidence that with aggressive memory optimization a cost-effective, high-performing model can be served at global scale on non-Nvidia silicon, albeit a smaller and slower model than the frontier. Two days after Flash, Z.ai released GLM-5.3 weights under an MIT-like license with an added clause requiring any business above $10B revenue to pass a Z.ai security review before commercial use — GLM-5.3-Flash carries no such clause.

Foreseeable misreading: GLM-5.3 still beats Flash on text benchmarks; Flash is the more *advanced* model in the sense that it has a new base, architecture and native vision, while GLM-5.3 is a highly capable fine-tune.
