---
type: observation
domain: [ai, machine-learning, reinforcement-learning]
confidence: 0.75
sources: 0
entities: [POPE, GRPO, Carnegie Mellon University, Qwen3-4B-Instruct-2507, AIME 2025, HMMT 2025]
refs: ['https://www.deeplearning.ai/the-batch/reinforcement-learning-with-hints']
---
# POPE: reinforcement learning with solution-prefix hints (CMU)

Carnegie Mellon researchers (Yuxiao Qu, Amrith Setlur, Virginia Smith, Ruslan Salakhutdinov, Aviral Kumar) introduced Privileged On-Policy Exploration (POPE), an LLM training method that pairs the RL algorithm GRPO with datasets that append the beginning (prefix) of a known solution as a hint, shown to the model both with and without the hint in equal ratio. The prefix helps the model discover solutions to hard problems where exploration normally fails. Fine-tuning Qwen3-4B-Instruct-2507 via POPE outperformed typical GRPO and supervised fine-tuning: on AIME 2025, 53.1% pass@1 / 82.6% pass@16 vs GRPO's 49.6% / 81.4%; on HMMT 2025, 37.8% / 67.5% vs GRPO's 31.0% / 63.8%. POPE requires problems with known solutions, inheriting that cost.
