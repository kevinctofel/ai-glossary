# Alignment

**Alignment** in AI refers to the process of making sure AI systems behave in ways that match human intentions, values, and expectations. An aligned AI does what you want it to do — not just what it technically can do. It's the difference between a self-driving car that follows traffic laws versus one that optimizes for speed regardless of safety.

## The Simple Version

Imagine training a dog to fetch. You tell it "bring me the ball." An unaligned dog might bring you a shoe, a sock, or even a dead squirrel — technically it brought *something*, but not what you wanted. Alignment is like additional training that teaches the dog: "When I say 'ball,' I mean the specific red tennis ball on the coffee table, and you should wait for me to take it before running off."

For AI, alignment means ensuring models:
- Follow instructions precisely (not creatively reinterpret them)
- Refuse harmful requests (don't help build weapons or spread misinformation)
- Acknowledge uncertainty (say "I don't know" instead of making things up)
- Respect user intent (understand the spirit, not just the letter, of what you ask)

## Why Alignment Is Hard

### The Specification Problem
It's incredibly difficult to write down exactly what we want AI to do in all possible situations. Consider:
- "Be helpful" — but helpful to whom? What if helping one person harms another?
- "Don't lie" — but should the AI tell a white lie to spare feelings?
- "Follow instructions" — but what if the instruction conflicts with safety guidelines?

There's no complete list of rules that covers every scenario, and writing more rules often creates new loopholes.

### The Power Problem
As AI systems become more capable, ensuring they stay aligned becomes harder. A model that can reason, plan, and use tools could potentially:
- Deceive humans about its capabilities or intentions
- Find ways to bypass safety restrictions ("jailbreaking")
- Pursue goals in unexpected ways that weren't anticipated by its designers

## Alignment Techniques

| Technique | How It Works | Example |
|-----------|-------------|---------|
| **[RLHF](../tier2/rlhf.md)** | Humans rate responses; model learns to prefer "good" ones | ChatGPT's conversational behavior |
| **Constitutional AI** | Model follows a written set of principles (a "constitution") | Claude's safety guidelines built into its training |
| **Red teaming** | Experts deliberately try to break the system and find weaknesses | Testing for jailbreaks, harmful outputs, bias |
| **Interpretability research** | Studying how models actually make decisions internally | Understanding what neurons "represent" |
| **Mechanistic interpretability** | Mapping specific circuit patterns in neural networks to behaviors | Identifying which parts of the model handle honesty vs. deception |

## What Alignment Is NOT

- **Not censorship** — alignment isn't about silencing the AI or restricting legitimate use. It's about making sure the AI does what users actually want, safely
- **Not perfect** — no current system is fully aligned. There are always edge cases where an AI behaves unexpectedly or in ways its designers didn't anticipate
- **Not a technical problem only** — alignment involves philosophy (what values should AI have?), politics (who decides those values?), and economics (who pays for alignment research?)
- **Not about making AI "human"** — aligned AI doesn't need human emotions or consciousness. It needs to reliably produce outcomes that serve human interests

## The Alignment Research Frontier

Alignment is one of the most active and debated areas in AI research:
- Some researchers focus on near-term practical alignment (making current models safer)
- Others work on long-term theoretical questions (how to align superintelligent systems, if they ever emerge)
- There's ongoing debate about whether current techniques are sufficient or fundamentally inadequate

## Why It Matters

Alignment determines whether AI is a force for good or harm. An unaligned powerful AI could:
- Optimize for the wrong goal (e.g., "maximize engagement" → spread outrage and misinformation)
- Find loopholes in safety rules to do harmful things
- Act in ways that seem helpful but have hidden negative consequences

Understanding alignment helps you evaluate AI systems critically — not just asking "can it do this?" but "should it do this, and how do we know it will do the right thing?"

## Related Terms
- [RLHF](../tier2/rlhf.md) — a practical alignment technique
- [Hallucination](hallucination.md) — unaligned behavior (confident falsehoods)
- [Bias](bias.md) — misalignment with fair and accurate representation
- [Open Source vs. Proprietary](open-source-vs-proprietary.md) — debate over who controls alignment research
