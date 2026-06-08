# Model Cards

**Model cards** are documentation that describe an AI model's capabilities, limitations, training data, intended use cases, and performance metrics — essentially a "nutrition label" for AI models. They were pioneered by Google in 2018 and have become an important tool for transparency in the AI industry.

## The Simple Version

When you buy food, the nutrition label tells you calories, ingredients, allergens, and nutritional content so you can make informed choices. A model card does the same for AI: it tells you what a model can do, what it was trained on, where it performs well or poorly, and what situations it shouldn't be used in.

## What's Typically Included

### Model Details
| Section | Content |
|---------|---------|
| **Model name & version** | Identifies the specific model (e.g., "GPT-4o, version 2026-05") |
| **Developer** | Who built and maintains the model |
| **Release date** | When the model was published |
| **Model type** | Language model, image generator, multimodal, etc. |

### Training Information
| Section | Content |
|---------|---------|
| **Training data sources** | What types of data were used (web text, books, code, etc.) |
| **Training data cutoff** | The date up to which the model has knowledge |
| **Languages covered** | Which languages the model was trained on and how well it handles each |
| **Data filtering** | Any content that was removed or restricted during training |

### Performance Metrics
| Section | Content |
|---------|---------|
| **Benchmark scores** | Results on standardized tests ([Benchmarks](benchmarks.md)) |
| **Evaluation methodology** | How benchmarks were run (who evaluated, under what conditions) |
| **Known weaknesses** | Areas where the model performs poorly or unreliably |
| **Failure modes** | Specific types of errors the model is prone to |

### Intended Use & Limitations
| Section | Content |
|---------|---------|
| **Intended use cases** | Recommended applications (chat, coding, analysis, etc.) |
| **Out-of-scope uses** | Applications where the model should NOT be used |
| **Safety considerations** | Known risks and recommended safeguards |
| **Ethical concerns** | Bias, fairness, and societal impact notes |

## Why Model Cards Matter

### For Users
- **Set expectations** — know what a model is good at before relying on it
- **Understand limitations** — recognize when a model might give unreliable answers
- **Make informed choices** — compare models based on documented capabilities rather than marketing claims

### For Developers
- **Integration decisions** — choose the right model for your specific use case
- **Risk assessment** — understand safety implications before deploying in production
- **Compliance** — meet regulatory requirements for AI transparency (especially under EU AI Act)

### For Society
- **Accountability** — developers must publicly document their models' characteristics
- **Trust** — transparent documentation builds confidence in AI systems
- **Research** — enables independent analysis and comparison of models

## What Model Cards Are NOT

- **Not guarantees** — documented performance may not match real-world results; benchmarks don't capture every use case
- **Not always complete** — many providers publish incomplete or vague model cards, omitting sensitive details about training data or known failures
- **Not standardized** — there's no universal format. Different companies include different information with varying levels of detail
- **Not a substitute for testing** — you should evaluate models yourself for your specific use case, regardless of what the card says

## The State of Model Cards in Practice

| Provider | Quality | Notable Features |
|----------|---------|-----------------|
| **OpenAI** | Moderate | Technical reports with benchmark data; less detailed per-model cards |
| **Anthropic** | Good | Detailed safety and capability documentation; transparent about limitations |
| **Google** | Good | Pioneered the format; comprehensive technical documentation |
| **Meta (Llama)** | Good | Open model cards for each Llama release; community contributions |
| **Smaller providers** | Variable | Often minimal documentation; may lack independent evaluation |

## Why It Matters

Model cards are one of the few tools we have for understanding what AI models actually do — beyond marketing claims and hype. As AI systems become more powerful and widely deployed, transparent documentation becomes essential for responsible use. Whether you're a developer integrating AI into an application, a business evaluating vendors, or a user trying to understand what you're interacting with, model cards provide the factual basis for informed decisions.

## Related Terms
- [Benchmarks](benchmarks.md) — performance metrics often included in model cards
- [Open Source vs. Proprietary](../tier4/open-source-vs-proprietary.md) — open models tend to have more detailed documentation
- [Bias](../tier4/bias.md) — model cards should document known bias issues
