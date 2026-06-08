# Hallucination

**Hallucination** in AI refers to when a model generates information that sounds plausible but is factually incorrect, fabricated, or not grounded in reality. The term comes from the medical definition — seeing or hearing things that aren't there — applied to language models producing confident-sounding falsehoods.

## The Simple Version

Imagine someone who read a lot of fiction and history books but never visited any of the places they wrote about. If you asked them about "the 18th-century coffeehouse in Prague where Mozart debated philosophy," they might give you a detailed, convincing description — complete with names, dates, and quotes — even though no such place or event ever existed. That's hallucination: confident, coherent, but completely made up.

## Why Hallucinations Happen

LLMs are designed to predict the next word in a sequence based on patterns they've learned. They're not fact-checking systems — they're pattern-matching engines. When asked about something they don't know:

1. The model recognizes the question format and structure
2. It searches its training data for similar patterns
3. It generates a response that *looks* like a correct answer (right tone, right format, plausible details)
4. But the specific facts may be invented because no real source matches exactly

## Types of Hallucinations

| Type | Description | Example |
|------|-------------|---------|
| **Factual** | Incorrect facts presented as truth | "The Eiffel Tower was built in 1889 for the World's Fair" ✓ vs. "Shakespeare wrote about quantum mechanics" ✗ |
| **Referential** | Making up people, places, or documents that don't exist | Citing a real-sounding paper that was never published |
| **Logical** | Reasoning errors that produce wrong conclusions despite correct premises | "All cats are mammals. Fluffy is a mammal. Therefore Fluffy is a cat." |
| **Instruction-following** | Ignoring or misinterpreting constraints in the prompt | Asked for 3 bullet points, gives 7 instead |

## How to Spot Hallucinations

- **Over-confidence** — AI states uncertain information with absolute certainty
- **Too-perfect details** — specific names, dates, and quotes that you can't verify
- **Internal contradictions** — the response contains facts that conflict with each other
- **Wikipedia test** — if a claimed fact doesn't appear anywhere on the internet, it's likely hallucinated
- **Source checking** — AI often cites papers or articles that don't exist

## Reducing Hallucinations

| Strategy | How It Helps |
|----------|-------------|
| **[RAG](../tier2/rag.md)** | Grounds responses in retrieved documents instead of pure memory |
| **Lower temperature** ([Temperature & Sampling](../tier1/temperature-sampling.md)) | Makes the model more deterministic and less creative |
| **Ask for sources** — prompt the model to cite where information came from | Makes hallucinations easier to detect (fake citations are obvious) |
| **Fact-checking step** — have a second system verify claims before presenting them | Adds a verification layer |
| **Acknowledge uncertainty** — train models to say "I don't know" when appropriate | Reduces confident falsehoods |

## What Hallucination Is NOT

- **Not always bad** — in creative writing, brainstorming, or ideation, hallucinations can be useful (generating novel ideas that happen to be wrong but spark real innovation)
- **Not unique to AI** — humans also "hallucinate" memories, misremember facts, and confidently state things we got wrong. AI just does it more visibly because it's fast and fluent
- **Not a sign of brokenness** — hallucination is an inherent property of how LLMs work (predictive text generation), not a bug that can be completely eliminated

## Why It Matters

Hallucination is the single biggest trust barrier for AI adoption. If you can't rely on an AI's answers to be true, it limits where and how you use it — especially in high-stakes contexts like healthcare, law, finance, or education. Understanding hallucination helps you:
- Know when to trust AI output and when to verify independently
- Design systems that minimize harmful hallucinations
- Set realistic expectations about what AI can reliably do

## Related Terms
- [Alignment](alignment.md) — training AI to be honest about uncertainty
- [RAG](../tier2/rag.md) — reducing hallucinations by grounding in real data
- [RLHF](../tier2/rlhf.md) — human feedback helps reduce confident falsehoods
- [Context Window](../tier1/context-window.md) — more context can reduce some types of hallucination
