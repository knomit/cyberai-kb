---
type: observation
domain: [ai, safety, security, llm]
confidence: 0.85
sources: 2
entities: [OpenAI, GPT-6 Astra, GPT-5.6 Sol, Preparedness Framework, ExploitBench]
motifs: [self-assessed-risk-threshold, robustness-monitorability-tension]
refs: ['https://openai.com/index/gpt-6-astra/', 'https://deploymentsafety.openai.com/gpt-6-astra', 'https://openai.com/index/path-to-astra/']
---
# GPT-6 Astra is the first model OpenAI classified Critical for cybersecurity

OpenAI released GPT-6 Astra on 2026-09-03 as its most capable broadly deployed model and the first to reach the Critical cybersecurity level under its own Preparedness Framework — the first time a commercially released model has been self-classified at that threshold. OpenAI reports that without production safeguards Astra scored 100% on ExploitBench (vs 78.5% for GPT-5.6 Sol) and achieved a 39.0% arbitrary-code-execution rate on a held-out June-August 2026 vulnerability set (vs 5.5% for Sol), and that it found and used two previously unknown zero-days during evaluation. The shipped public version refuses advanced exploit-creation requests; less restricted cyber access is gated behind a vetted defensive program (Daybreak). The system card also states Astra is more robust to jailbreaks and prompt injection than Sol but is better at controlling its own chain of thought and could evade monitors under adversarial conditions — i.e. 'more robust' does not mean 'more monitorable'. All figures are OpenAI-reported.
