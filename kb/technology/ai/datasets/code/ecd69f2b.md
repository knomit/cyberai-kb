---
type: observation
domain: [technology, ai, datasets]
confidence: 0.8
sources: 1
entities: [Hugging Face, The Stack v3, Anton Lozhkov, BigCode, GitHub, StarCoder2]
refs: ['https://huggingface.co/datasets/HuggingFaceCode/stack-v3-train', 'https://huggingface.co/spaces/HuggingFaceCode/in-the-stack', 'https://www.deeplearning.ai/the-batch/issue-365']
---
# Hugging Face released The Stack v3, the largest up-to-date open dataset of source code

Anton Lozhkov and colleagues at Hugging Face released The Stack v3, a snapshot of public GitHub code for pretraining LLMs. Two releases: stack-v3-train (15.9 TB, ~4.9 trillion tokens, 713 programming languages from 173 million repositories, deduplicated/quality-filtered/PII-scrubbed) and stack-v3-full (113.7 TB, 770 languages from 224 million repositories, raw). Knowledge cutoff Aug 7, 2025. Licensed under Open Data Commons Attribution (ODC-BY) v1.0. Unlike The Stack v2 (which pulled from Software Heritage and delivered only file identifiers), v3 crawled GitHub directly and delivers whole repositories with their files, so models can learn cross-file structure needed by agentic coding assistants. Pipeline skipped files >5MB, binaries, and forks with <5 stars (43.9B files crawled); used ScanCode for license detection, cross-language MinHash dedup at ≥70% overlap, StarCoder2 quality filters, and StarPII to redact personal information. Developers can check inclusion and opt out via the 'in-the-stack' tool. Caveats: automated license labels are error-prone, no-license files grant no reuse rights, and the corpus may contain leaked secrets or malicious code.
