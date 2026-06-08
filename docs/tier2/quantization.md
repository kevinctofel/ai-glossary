# Quantization

**Quantization** is a technique for reducing the precision of numbers used in AI models, making them smaller and faster to run without significantly sacrificing quality. It's like compressing an image — you lose some detail but keep the overall picture intact, while using much less storage space.

## The Simple Version

AI models use huge numbers (floating-point values with lots of decimal places) to represent their knowledge. Quantization shrinks these numbers by rounding them to fewer digits — for example, going from 16-bit precision (like writing "3.14159265") down to 8-bit ("3.14") or even 4-bit ("3.1"). The model gets smaller and faster, but still works well enough for most tasks.

## Why Quantize?

| Metric | Full Precision (FP16) | Q8 (8-bit) | Q4 (4-bit) |
|--------|----------------------|-----------|-----------|
| Model size | 100% | ~50% smaller | ~75% smaller |
| Speed | Baseline | ~2x faster | ~3-4x faster |
| Quality loss | None | Minimal (often <1%) | Small but noticeable |
| Can run on consumer hardware? | Sometimes | Usually yes | Almost always |

The main benefit: quantization makes powerful AI models runnable on everyday computers instead of requiring expensive data center GPUs. This is why you can run LLMs locally on your laptop — they're almost certainly running in a quantized format.

## Common Quantization Formats

### FP16 (Half Precision)
- 16-bit floating point
- Minimal quality loss
- Still fairly large models
- Used by many cloud APIs

### INT8 (8-bit Integer)
- 8-bit whole numbers
- ~50% size reduction
- Very small quality impact
- Good balance of speed and accuracy

### Q4_K_M / Q5_K_M (GGUF formats)
- Mixed precision quantization (different parts of the model get different bit depths)
- Developed for the llama.cpp ecosystem
- "K" stands for "k-quants" — a smart approach that quantizes less important weights more aggressively
- Q4 is popular for running models on CPUs; Q5/Q6 for better quality when you have some GPU

### NF4 (4-bit Normal Float)
- Specialized 4-bit format designed specifically for AI
- Used inQLoRA ([Fine-tuning](fine-tuning.md)) for efficient model adaptation
- Can represent values more efficiently than regular INT4 for neural network distributions

## What Quantization Is NOT

- **Not compression** — it's not like ZIP files. Quantization changes the actual number representation, not just encoding
- **Not lossless** — you always lose some precision. The art is finding the right balance between size and quality
- **Not reversible** — once quantized, you can't recover the original full-precision model from the quantized version

## Trade-offs to Consider

| When to use higher bits (Q6/Q8) | When to use lower bits (Q3/Q4) |
|--------------------------------|-------------------------------|
| You need maximum accuracy | You're running on limited hardware |
| The task is complex/nuanced | Simple tasks (chat, summarization) |
| You have GPU acceleration | CPU-only inference |
| Model size isn't a constraint | Storage/bandwidth is limited |

## Why It Matters

Quantization is what made the current wave of accessible AI possible. Without it, running even modest-sized models would require expensive enterprise hardware. With quantization, you can run powerful models on a laptop, phone, or cheap cloud instance. As models get larger (100B+ parameters), quantization becomes not just convenient but essential — a 100B model in full precision might need 200GB of RAM; quantized to Q4, it fits in ~50GB.

## Related Terms
- [Parameters](../tier1/parameters.md) — what gets quantized
- [Fine-tuning](fine-tuning.md) — QLoRA uses quantization for efficient fine-tuning
- [Inference vs. Training](../tier1/inference-vs-training.md) — quantization mainly affects inference speed
- [LLM (Large Language Model)](llm.md) — models that benefit most from quantization
