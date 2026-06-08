# Temperature & Sampling

**Temperature** and **sampling** are settings that control how creative or predictable an AI's responses will be. They determine whether the model picks the most likely next word or takes more risks.

## The Simple Version

Imagine you're playing a game where you need to pick the next word in a sentence. You have a list of options ranked by likelihood:

| Word | Likelihood |
|------|-----------|
| "cat" | 40% |
| "dog" | 25% |
| "bird" | 15% |
| "fish" | 10% |
| "hamster" | 5% |
| "dragon" | 3% |
- **Low temperature (0.1)** — You almost always pick "cat." Very predictable, very consistent.
- **Medium temperature (0.7)** — You usually pick "cat" or "dog," sometimes "bird." Balanced.
- **High temperature (1.5)** — You might pick "hamster" or even "dragon." Creative but risky.

Temperature controls how much weight you give to the less likely options.

## How It Works Mathematically (Simplified)

The model calculates probabilities for every possible next word. Temperature adjusts those probabilities:
- **Low temperature** sharpens the distribution — the most likely option becomes even more dominant
- **High temperature** flattens the distribution — less likely options get a bigger chance
- **Temperature of 0** means always pick the single most likely word (deterministic)

## Sampling Methods

Sampling is *how* the model picks from the probability distribution. Common methods:

### Greedy Decoding (temperature = 0)
Always picks the highest-probability word. Results are consistent but can be repetitive and boring.

### Top-K Sampling
Only considers the K most likely words, then picks randomly from those.
- **Top-K = 10** — very focused, safe choices
- **Top-K = 50** — more variety, still reasonable

### Top-P (Nucleus) Sampling
Only considers words that make up the top P% of probability mass.
- **Top-P = 0.9** — considers words until 90% of probability is covered
- More adaptive than Top-K because it adjusts to how confident the model is

## Practical Temperature Guide

| Temperature | Best For | Risk |
|------------|---------|------|
| **0.0 – 0.3** | Factual answers, code generation, math | Repetitive, predictable output |
| **0.4 – 0.7** | General conversation, summaries, analysis | Balanced — good default range |
| **0.8 – 1.2** | Creative writing, brainstorming, storytelling | May drift off-topic or hallucinate |
| **1.3 – 2.0** | Poetry, wild ideation, art prompts | High risk of nonsense or incoherence |

## What Temperature Is NOT

- **Not a creativity dial on the model itself** — it doesn't make the model "more creative." It just changes how it picks from what it already knows
- **Not about intelligence** — a low temperature response isn't "smarter," just more conservative
- **Not permanent** — you can change temperature for each request. The same model can be factual at 0.2 and creative at 1.0

## Why This Matters for You

### When Using AI Services
Many services let you adjust temperature:
- **Writing code or getting facts** → keep it low (0.1–0.3)
- **Brainstorming ideas** → medium (0.7–0.9)
- **Creative writing** → higher (1.0–1.5)

### When Running Models Locally
You control temperature directly, so you can experiment and find what works for your use case. This is one of the most impactful settings you can tweak.

## Related Terms
- [Prompts & Prompt Engineering](prompts.md) — how you structure input affects output quality
- [Tokens & Tokenization](tokens-tokenization.md) — each word picked is a token
- [Inference vs. Training](inference-vs-training.md) — temperature matters during inference (when generating responses)
