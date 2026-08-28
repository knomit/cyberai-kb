---
type: concept
domain: [llm-architecture, long-context]
confidence: 0.75
sources: 1
entities: [DeepSeek, DeepSeek-V4, DeepSeek-V3.2]
refs: ['https://api-docs.deepseek.com/news/news260813', 'https://www.deeplearning.ai/the-batch/issue-368']
---
# DeepSeek's hybrid attention uses 27% of the compute and 10% of the KV memory of V3.2 at 1M tokens

DeepSeek-V4's hybrid attention alternates between two kinds of attention layers. Both compress the keys and values the model stores while reading input, but one additionally attends only to a selected subset of tokens. For 1 million tokens of input, the model uses only 27 percent of the computation and 10 percent of the memory for stored keys and values that DeepSeek-V3.2 required. The V4 preview was pretrained on more than 32 trillion tokens, then fine-tuned as 10 separate domain specialists and merged back into one model via on-policy distillation.
