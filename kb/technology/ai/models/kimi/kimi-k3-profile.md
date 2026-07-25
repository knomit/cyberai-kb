---
type: observation
domain: [technology, ai, llm, architecture]
confidence: 0.78
sources: 2
evidence_weight: 0.7560975609756098
entities: [Moonshot AI, Kimi K3, mixture-of-experts]
refs: ['https://info.deeplearning.ai/kimi-k3-redraws-the-open-frontier', 'https://www.akashbajwa.co/p/sparse-by-design']
---
# Moonshot AI introduced Kimi K3, a 2.8T-parameter sparse open-weights model

Moonshot AI introduced Kimi K3, a 2.8 trillion-parameter mixture-of-experts vision-language model that activates 16 of 896 experts (~50B parameters) per token — sparse by design, so active-parameter count per token stays low despite total parameter growth versus predecessors. It supports up to 1M-token input/output, was available immediately via API with weights promised by July 27, 2026 (which would make it the largest known open-weights model), ranked third on Artificial Analysis's Intelligence Index (57) and first among open models, and ranked first on Arena.ai's Code Arena WebDev leaderboard. Priced at $3.00/$0.30/$15.00 per million input/cached/output tokens. Efficiency comes from Kimi Delta Attention (linear attention in 3 of every 4 layers) and Attention Residuals, making training ~2.5x more efficient than its predecessor.
