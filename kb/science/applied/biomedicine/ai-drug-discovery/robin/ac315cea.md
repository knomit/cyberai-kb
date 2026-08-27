---
type: observation
domain: [science, biomedicine, ai]
confidence: 0.78
sources: 1
entities: [Robin, FutureHouse, dAMD, Y-27632, Ripasudil, RPE phagocytosis, Crow, Falcon, Finch]
refs: ['https://info.deeplearning.ai/ai-overviews-land-google-in-hot-water-gpt-live-puts-reasoning-in-the-background-how-to-tell-if-your-model-is-manipulative']
---
# FutureHouse's Robin agent proposed repurposed drugs for macular degeneration

Researchers from FutureHouse, University of Oxford, and Fordham University (Ali Essam Ghareeb, Benjamin Chang, and colleagues) released Robin, an open-source (Apache 2.0) agent that proposes existing drugs to treat a given disease nearly autonomously — humans only name the disease and run the AI-proposed lab experiments. Robin iteratively identifies disease mechanisms, designs experiments, finds existing drugs, then analyzes human-run experimental results. It uses OpenAI GPT o4-mini for most language tasks and Claude 3.7 Sonnet to rank experimental designs and drug reports; it relies on literature agents Crow and Falcon and data-analysis agent Finch. For dry age-related macular degeneration (dAMD), Robin hypothesized boosting RPE phagocytosis and identified two effective compounds: research compound Y-27632 (~2x increase in RPE phagocytosis) and Ripasudil, a glaucoma drug approved in Japan (1.89x increase). The drugs were tested only on isolated human eye cells, not on patients.
