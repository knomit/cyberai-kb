---
type: methodology
domain: [ai, infrastructure, serving]
confidence: 0.75
sources: 1
entities: [LMSYS, DeepSeek-V4-Pro, H20]
refs: ['https://www.lmsys.org/blog/2026-08-19-deepseek-v4-pro-engine-optimization-h20']
---
# Serving-profile selection for frontier models should start from workload and SLO, not hardware specs

LMSYS published a methodology for serving DeepSeek-V4-Pro arguing that serving profiles should not be selected from hardware specifications or isolated benchmarks alone. The recommended approach starts from the workload, SLO, context length, and concurrency, then uses profiling to identify the binding resource and translates that into concrete topology and execution-path decisions — a repeatable way for AI infrastructure teams to build frontier-model serving systems under diverse resource constraints.
