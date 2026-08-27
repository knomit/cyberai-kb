---
type: observation
domain: [security, hardware, gpu]
confidence: 0.85
sources: 1
entities: [GPUThor, NVIDIA, University of Toronto, RTX A6000, Rowhammer, CUDA]
refs: ['https://thehackernews.com/2026/08/gputhor-rowhammer-defeats-ecc-on-nvidia.html']
---
# GPUThor Rowhammer attack defeats ECC on NVIDIA workstation GPUs

Researchers at the University of Toronto disclosed GPUThor, a Rowhammer attack against NVIDIA workstation GPUs with GDDR6 memory that defeats error correction codes (ECC) — the mitigation NVIDIA recommends against GPU Rowhammer — enabling denial of service and privilege escalation to a host root shell. Hammering four DRAM banks for 24 hours each on four Ampere-class cards induced bit flips on every card. Confirmed vulnerable: RTX A6000 (48GB), RTX A5000 (24GB), RTX A4500 (20GB), and RTX A4000 (16GB). The attack requires only the ability to launch an unprivileged CUDA kernel on the target GPU, either as a co-tenant on a shared card or as untrusted code on a single-tenant machine. Recommended mitigations: avoid cross-tenant GPU sharing, monitor ECC error counters, and restrict untrusted CUDA workloads.
