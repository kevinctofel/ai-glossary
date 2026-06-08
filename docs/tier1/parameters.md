# Parameters

**Parameters** are the internal settings of an AI model that get adjusted during training. They're essentially the model's "knowledge" — how it understands language, patterns, and relationships between concepts.

## The Simple Version

Imagine a radio with 100 knobs. Each knob controls a different aspect of the sound. When you tune all 100 knobs to the right positions, you get clear music instead of static. AI parameters are like those knobs — billions of them, adjusted during training so the model produces useful output instead of gibberish.

## What Parameters Actually Are

At the mathematical level, parameters are numbers stored in the model's weights and biases. They determine:
- How strongly certain patterns trigger responses
- Which words tend to follow other words
- How concepts relate to each other
- The "style" or "voice" of the output

When you see a model described as having "7 billion parameters" or "175 billion parameters," that's counting how many adjustable numbers are in the model.

## More Parameters ≠ Smarter (Always)

This is a common misconception. Here's why:

| | More Parameters | Fewer Parameters |
|--|----------------|-----------------|
| **Potential** | Can learn more complex patterns | Limited capacity for complexity |
| **Data needed** | Needs massive datasets to train properly | Can work with less data |
| **Speed** | Slower to run (more math per response) | Faster to run |
| **Memory** | Needs more RAM/VRAM to load | Fits on smaller hardware |
| **Quality** | Only better if trained well and on good data | Can be surprisingly capable with right training |

A 7B parameter model trained on excellent, focused data can outperform a 175B parameter model trained on noisy, generic data.

## What Parameter Count Tells You

- **Rough capacity indicator** — more parameters generally means the model can handle more complex tasks
- **Hardware requirement** — bigger models need more RAM/VRAM to run
- **Not a quality guarantee** — training data quality and methodology matter just as much

## Practical Implications

### For Running Models Locally
- A 7B parameter model in Q4 quantization needs ~5GB of RAM
- A 13B parameter model needs ~8GB
- A 70B parameter model needs ~40GB+
- Your hardware limits which models you can run

### For API Costs
Larger models (more parameters) typically cost more per token because they require more compute to run.

## Related Terms
- [Training](inference-vs-training.md) — where parameters get set during training
- [Quantization](tier2/quantization.md) — reducing parameter precision to save memory
- [Tokens & Tokenization](tokens-tokenization.md) — what the model processes using its parameters
