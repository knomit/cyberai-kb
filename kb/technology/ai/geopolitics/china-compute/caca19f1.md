---
type: observation
domain: [ai, geopolitics, chips, china]
confidence: 0.75
sources: 3
entities: [Huawei, DeepSeek, Nvidia, SMIC, TSMC]
refs: [kb/technology/ai/geopolitics/8aa8aa29.md, 'https://www.tomshardware.com/tech-industry/artificial-intelligence/deepseek-research-suggests-huaweis-ascend-910c-delivers-60-percent-nvidia-h100-inference-performance', 'https://tokenmix.ai/blog/deepseek-v4-release-delay-huawei-chip-2026']
---
# Huawei Ascend 910C at 60% of H100 inference performance mid-2026 — training still requires Nvidia

As of mid-2026, DeepSeek researchers report the Huawei Ascend 910C delivers approximately 60% of Nvidia H100 inference throughput — a 40% gap remaining. DeepSeek claims parity for V4 inference on Ascend in their own benchmarks, but this is self-reported and lacks independent third-party verification.

DeepSeek spent Q1 2026 on kernel-level adaptations to run V4 efficiently on Huawei's Da Vinci architecture (fundamentally different from CUDA). The Ascend 910C is manufactured on SMIC's 7nm process vs. H100's TSMC 4nm — a process node disadvantage that constrains peak throughput.

Training remains the critical gap: DeepSeek still used Nvidia GPUs for the bulk of V4 training. The Huawei CANN software stack has not closed the kernel optimization depth gap for training workloads. Inference is more tractable because it is less software-ecosystem-dependent than training.

Relevance to hypothesis kb/technology/ai/geopolitics/8aa8aa29.md: that hypothesis requires Ascend systems to reach within 30% of H100 inference on 2+ benchmarks by Q4 2027. Current gap is 40% on inference (per DeepSeek's own numbers), with training parity much further off. Progress is real but the 30% threshold has not yet been crossed, and the training gap remains the structural load-bearing unknown.
