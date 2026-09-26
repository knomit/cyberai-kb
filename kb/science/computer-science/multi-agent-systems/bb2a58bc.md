---
type: observation
domain: [ai, research]
confidence: 0.75
sources: 1
entities: [Carnegie Mellon University, Xuecheng Liu, Daman Arora, Qwen3]
refs: ['https://info.deeplearning.ai/what-stage-is-your-project']
---
# CMU's Message Passing Language Models let parallel agent threads communicate directly, removing a coordinator bottleneck

Researchers at Carnegie Mellon University (led by Xuecheng Liu and Daman Arora) proposed Message Passing Language Models (MPLMs), an agentic harness in which an LLM distributes sub-problems among separate threads (each running its own copy of the LLM) that communicate directly with one another via commands to start threads, send results to specific threads, wait for replies, or stop threads -- removing the need for a central coordinator thread that can otherwise become a bottleneck as tasks wait on it. The authors trained Qwen3-0.6B-Base on text traces from programs solving 3-SAT and Sudoku puzzles this way. On 9x9 Sudoku, MPLM solved 100% of puzzles in about 15 seconds versus a coordinator-based parallel-agent method solving 93% in about 60 seconds; MPLM's per-thread token usage also grew more slowly as grid size increased, letting it solve 72% of 25x25 Sudoku grids where the coordinator-based and single-thread methods hit context/compute limits before finding solutions. On 3-SAT problems (8-20 variables), MPLM's accuracy (~92%) was roughly even with the coordinator-based method (~91%) but was faster on average, sometimes up to 2.5x faster on individual examples because a thread that found a solution could stop the others. Limitation: MPLM requires knowing in advance which threads must communicate with which, so it works best on problems (like Sudoku and 3-SAT) with a fixed, easily-derived communication pattern; for open-ended problems the pattern may require careful prompting or extra training to discover. Larger models (Qwen3-30B-A3B, Qwen3.6-35B-A3B) also showed improved accuracy and roughly 2x lower average latency using this method on the LongBench-v2 long-context reasoning benchmark, suggesting the approach generalizes beyond puzzles, though effects appeared stronger on smaller models.
