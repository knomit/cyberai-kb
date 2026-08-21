---
type: concept
domain: [ai, systems, gpu-inference]
confidence: 0.85
sources: 1
entities: [PagedAttention, vLLM]
refs: ['https://thegustafson.com/blog/paged-attention']
---
# PagedAttention applies OS virtual-memory paging to the LLM KV cache

The KV cache is a per-request store of attention keys and values that lets a model avoid recomputing them at every decoding step. It grows linearly with sequence length, and at long contexts it consumes more GPU memory than the model weights themselves, making it a scarce resource. A naive contiguous KV cache wastes substantial memory through fragmentation and over-allocation.

PagedAttention addresses this by implementing virtual-memory-style paging for the KV cache — storing it in non-contiguous fixed-size blocks — in a way that attention kernels can still operate on efficiently.
