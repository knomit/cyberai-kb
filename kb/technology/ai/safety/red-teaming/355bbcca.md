---
type: observation
domain: [ai-safety, security, prompt-injection]
confidence: 0.8
sources: 2
origin: discovered
entities: [OpenAI, GPT-Red, GPT-5.6 Sol]
refs: ['https://openai.com/index/unlocking-self-improvement-gpt-red/', 'https://thehackernews.com/2026/07/openais-gpt-red-automates-prompt.html']
---
# OpenAI's GPT-Red automates prompt-injection red-teaming

OpenAI disclosed GPT-Red, an internal automated red-teaming model that iteratively generates adversarial prompts to discover prompt-injection vulnerabilities at scale. It operates like a human red-teamer: sends a prompt, observes the target model's response, and iterates toward a malicious goal (e.g. exfiltrating sensitive data to an external server). OpenAI states it uses GPT-Red to adversarially train GPT-5.6, and reports that incorporating GPT-Red's attacks into training reduced failures on a difficult prompt-injection benchmark by roughly sixfold for GPT-5.6 Sol. OpenAI also says its previous models are highly vulnerable to GPT-Red's attacks.
