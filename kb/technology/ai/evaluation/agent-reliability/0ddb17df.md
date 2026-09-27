---
type: concept
domain: [ai-evaluation, agents]
confidence: 0.7
sources: 1
entities: [IBM Research, ALTK-Evolve]
motifs: [run-to-run-variance, single-sample-overclaim]
refs: ['https://huggingface.co/blog/ibm-research/altk-evolve-consistency']
---
# ALTK-Evolve targets the inconsistency gap where agent task success drops across repeated runs

IBM Research's ALTK-Evolve introduces Consistency Guidelines to address the 'inconsistency gap' — the phenomenon where a model's task success rate drops significantly across repeated runs of the same task. The practical consequence for agent evaluation: a single successful run is not evidence of reliable capability, and benchmarks reporting best-of-N or single-run success overstate deployable performance.
