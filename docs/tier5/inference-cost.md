# Inference Cost

**Inference cost** is the expense of running a trained AI model to generate responses — essentially "using" the model rather than building it. While training costs millions, inference happens constantly and adds up across billions of daily requests. Understanding inference cost helps you budget for AI usage and choose the right approach for your needs.

## The Simple Version

Training is like building a factory (huge upfront cost). Inference is like running that factory every day to produce products (ongoing cost per unit). For AI:
- **Training** = one-time cost of teaching the model ($10M-$1B+)
- **Inference** = ongoing cost each time someone uses it (cents to dollars per request)

Most AI spending is actually inference, not training — because models are used millions of times daily after being trained once.

## How Inference Cost Is Calculated

### Token-Based Pricing
Most API providers charge per token (word fragments):

| Component | What It Counts | Example |
|-----------|---------------|---------|
| **Input tokens** | Your prompt + conversation history | "Explain quantum physics in simple terms" = ~8 tokens |
| **Output tokens** | The model's response | A 200-word answer ≈ 250-300 tokens |

### Typical Pricing (as of mid-2026)

| Model Tier | Input Cost (per 1K tokens) | Output Cost (per 1K tokens) | Example Use |
|-----------|--------------------------|---------------------------|-------------|
| **Small/fast** | $0.001 - $0.005 | $0.002 - $0.01 | Simple tasks, autocomplete |
| **Mid-range** | $0.003 - $0.015 | $0.006 - $0.03 | General-purpose chat |
| **Large/smart** | $0.01 - $0.05 | $0.02 - $0.15 | Complex reasoning, analysis |

### Real-World Cost Examples

| Task | Approximate Tokens | Estimated Cost (mid-tier model) |
|------|-------------------|-------------------------------|
| Short answer (3 sentences) | ~100 input + 150 output | $0.002 - $0.004 |
| Email draft | ~80 input + 400 output | $0.006 - $0.012 |
| Code review (full file) | ~3,000 input + 500 output | $0.04 - $0.08 |
| Long document analysis | ~10,000 input + 1,000 output | $0.15 - $0.30 |
| Multi-turn conversation (20 messages) | ~5,000 input + 2,000 output | $0.10 - $0.25 |

## Reducing Inference Costs

### Strategy | How It Works | Savings Potential |
|-----------|-------------|-------------------|
| **Use smaller models** for simple tasks | Not every task needs the smartest model | 50-90% cost reduction |
| **Cache responses** for identical prompts | Don't re-run the same query | Near-zero cost for repeated queries |
| **Stream responses** and stop early | If you get what you need in 100 tokens, don't generate 1000 | 50-90% on long outputs |
| **Reduce context window** usage | Send only relevant conversation history | Fewer input tokens = cheaper |
| **Batch requests** | Group multiple prompts into one API call | Some providers offer batch discounts |
| **Run locally** with quantized models ([Quantization](../tier2/quantization.md)) | No per-token fees; just electricity and hardware | Free after hardware investment |

## Local vs. Cloud Inference Cost Comparison

| Factor | Cloud API | Local (Your Computer) |
|--------|-----------|----------------------|
| **Per-use cost** | Cents to dollars per request | Near-zero (just electricity) |
| **Upfront cost** | None (pay as you go) | GPU/NPU hardware ($500-$4,000+) |
| **Break-even point** | Depends on usage volume | ~10K-50K requests depending on model size |
| **Scalability** | Unlimited (provider handles load) | Limited by your hardware |
| **Privacy** | Data leaves your computer | Full data stays local |

## What Inference Cost Is NOT

- **Not fixed** — prices drop as models improve and competition increases. Today's expensive model may be tomorrow's cheap one
- **Not just about the model** — infrastructure, networking, and software overhead add to total cost beyond raw token pricing
- **Not the only cost factor** — development time, error handling, and user experience often matter more than raw inference costs

## Why It Matters

Inference cost determines whether AI is economically viable for your use case. A feature that costs $0.01 per use might be fine for a premium product but impossible for a free consumer app. Understanding these costs helps you:
- Design AI features that are sustainable at scale
- Choose between cloud and local deployment
- Set realistic pricing for AI-powered products
- Optimize prompts and workflows to minimize waste

## Related Terms
- [Compute](compute.md) — the hardware behind inference cost
- [APIs](apis.md) — how most people pay for inference
- [Quantization](../tier2/quantization.md) — making local inference cheaper and faster
