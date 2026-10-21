---
type: observation
domain: [ai, inference]
confidence: 0.75
sources: 1
entities: [DeepSeek, DeepInfer, DeepSeek-V4.1-Flash]
refs: ['https://github.com/deepseek-ai/DeepInfer', 'https://zhuanlan.zhihu.com/p/2095560295930508953']
---
# DeepSeek DeepInfer repo: offline inference for DeepSeek-V4.1-Flash

DeepSeek's DeepInfer GitHub repo is a version of the inference framework behind its large-scale production services, for offline inference. It runs DeepSeek-V4.1-Flash on NVIDIA SM100 GPUs or Huawei Ascend 950 NPUs. A KV cache system, VE/Prefill/Decode disaggregation and load balancing across data-parallel replicas are still required for a complete serving stack and are not included. A linked write-up says DeepSeek processes 155 trillion tokens per day per cluster and earns $38 revenue per GPU-hour (figures per that write-up).
