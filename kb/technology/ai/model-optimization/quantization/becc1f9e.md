---
type: observation
domain: [ai, quantization, inference]
confidence: 0.75
sources: 1
entities: [Unsloth, GGUF]
refs: ['https://unsloth.ai/docs/basics/dynamic-3.0-ggufs']
---
# Unsloth Dynamic 3.0 GGUFs improve quantized accuracy up to 10% at equal model size

Unsloth released Dynamic 3.0 GGUFs, improving accuracy over previous quantization methods while maintaining model size. The update uses a refined imatrix calibration dataset for better multilingual performance and deliberately avoids quantization-aware training (QAT) to reduce overfitting risk. Unsloth reports up to 10% better top-1% accuracy in smaller quant sizes plus substantial disk space savings.
