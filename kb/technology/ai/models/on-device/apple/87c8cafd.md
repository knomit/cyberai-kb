---
type: observation
domain: [ai, on-device, apple]
confidence: 0.8
sources: 0
entities: [Apple, AFM 3, Google Gemini, iPhone 17]
refs: ['https://info.deeplearning.ai/a-new-generation-studies-ai-apples-recipe-for-on-device-models-glm5.2-tackles-open-ended-problems']
---
# Apple AFM 3 introduces on-device model using Instruction-Following Pruning

Apple announced the third generation of Apple Foundation Models (AFM 3), built in collaboration with Google and distilled from unspecified Google Gemini models. AFM 3 Core Advanced runs on-device with a modified mixture-of-experts transformer (20 billion total parameters, 1-4 billion active). Instead of in-model routing layers, it uses Instruction-Following Pruning—a separate transformer selects which experts to activate across multiple tokens, enabling the model to be stored in flash memory and run faster than typical same-size MoE models. It will ship in fall 2026 with OS updates to Macs and iPhone 17 Pro/Max/Air, supporting text, image, and speech I/O across 25 languages. Apple struck its multi-year Gemini agreement with Google in January 2026.
