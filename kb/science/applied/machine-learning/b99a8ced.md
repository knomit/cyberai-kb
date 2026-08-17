---
type: synthesis
domain: [ai, evaluation, research-automation]
confidence: 0.7
sources: 1
evidence_weight: 0.6153846153846154
entities: [DiG-bench, Faraday, Inherent, Juergen Schmidhuber, Opus 5, Fable 5, GPT-5.5]
refs: ['kb://d88770a51516/kb/science/applied/machine-learning/benchmarks/4a2813ee.md', 'kb://d88770a51516/kb/science/applied/machine-learning/ai-for-science/0ac12ef7.md']
---
# 2026 AI evaluation is shifting from task performance to autonomous discovery, with small post-trained supervisors as one lever

Two mid-2026 research artifacts illustrate a shift in how frontier AI is measured and improved: away from performance on specified tasks and toward the capacity to discover what the task even is.

Measurement side — DiG-bench (Discovery in Games) is a benchmark of 70 handcrafted, purely text-based games in which both the rules and the objective are hidden and must be uncovered through interaction. 21 games are public and the rest are held back to prevent training contamination; games span seven difficulty tiers with 2 to 34 available actions per step, and every game has been beaten by at least one human. Opus 5 and Fable 5 running in Claude Code are the best overall models, followed by GPT-5.5; only Opus 5 and Fable 5 beat any Tier 7 tasks (score 0.2), while Opus 5, GPT-5.5 and Kimi K3 solved some Tier 6 tasks with a harness, and GLM-5.2 and Gemini 3.1 Pro reached some Tier 4 levels. Authors include Juergen Schmidhuber, with affiliations at Thinking About Thinking, Oxford, Princeton, KAUST, Swiss AI Lab, Inria and MIT.

Improvement side — Inherent's Faraday is a 27B supervisory model post-trained on Qwen-3.6-27B that sits on top of large proprietary frontier models and drives them (via OpenAI Codex as the underlying coding agent) to do better science. It trains on Replica, a dataset of 100 ML and AI-for-science papers published 1990–2026 converted into 310 replication tasks by knocking out individual results, with Claude Opus 4.7 generating per-task rubrics from a meta-rubric and a Codex-based judge supplying reward and per-turn credit assignment for a modified GRPO. Faraday+Codex exceeded standard Opus 4.8 and GPT-5.5 on 73% of in-distribution ML tasks and 60% of held-out AI-for-science tasks by the rubric-based judge.

The common thread: both target the same latent capability — autonomously working out what to investigate in an underspecified situation — and both show that a scaffold or harness around a model materially changes measured capability (DiG-bench tiers 6 and 7 were only reached with a harness; Faraday's gains come from an outer supervisory loop rather than a larger base model).

WHAT THIS DOES NOT MEAN: neither result shows frontier models have human-level discovery ability — on DiG-bench, individual humans reached 100% on tests where the best models score 0.2 at Tier 7. Faraday's results are judged by a rubric-based LLM judge, not by independent reproduction, and the comparison is against 'standard' Opus 4.8 and GPT-5.5 rather than those models with comparable scaffolding.
