# Compute (AI Compute)

**Compute** in AI refers to the processing power needed to train and run AI models — essentially the CPUs, GPUs, and specialized chips that do the mathematical work behind every AI operation. It's the "engine" that turns algorithms into intelligence, and it's one of the most scarce and expensive resources in the AI industry.

## The Simple Version

Training an AI model is like solving a puzzle with billions of pieces simultaneously. Each piece requires complex math (multiplying huge matrices of numbers). Compute is the hardware that does these calculations — and the more powerful the compute, the faster and larger the puzzles you can solve.

Think of it this way:
- **CPU** = a smart calculator doing one thing at a time
- **GPU** = thousands of simpler calculators working in parallel
- **AI accelerator (TPU, NPU)** = specialized calculators designed specifically for AI math

## Types of Compute Hardware

### GPUs (Graphics Processing Units)
Originally designed for rendering video game graphics, GPUs turned out to be excellent for AI because both tasks involve massive parallel math:

| GPU Type | Use Case | Example |
|----------|----------|---------|
| **Consumer** (RTX 4090) | Running smaller models locally, fine-tuning | $1,600-$2,000 per card |
| **Data center** (H100, H200) | Training large models, serving APIs | $30,000-$40,000+ per card |
| **Multi-GPU systems** | Training very large models (hundreds of GPUs) | Entire server racks with 8-16 GPUs |

### Specialized AI Chips
Companies have built chips optimized specifically for AI workloads:

| Chip | Developer | Advantage |
|------|-----------|----------|
| **TPU** (Tensor Processing Unit) | Google | Optimized for Google's ML framework; used in Google Cloud |
| **NPU** (Neural Processing Unit) | AMD, Apple, Qualcomm | Low-power AI acceleration for edge devices (phones, laptops) |
| **Trainium** | AWS (Amazon) | Cost-optimized for training on AWS infrastructure |

### The Strix Halo Context
On your AMD Ryzen AI MAX+ 395 APU, the NPU and integrated GPU handle AI workloads locally. This is "edge compute" — running AI on the device itself rather than sending data to a cloud server. It's slower than data center GPUs but offers privacy, no API costs, and works offline.

## Training vs. Inference Compute

| Aspect | Training | Inference |
|--------|----------|-----------|
| **When** | Building/teaching the model | Using the trained model |
| **Compute intensity** | Extremely high (weeks/months on hundreds of GPUs) | Moderate (milliseconds per response) |
| **Hardware** | Data center GPUs/TPUs with massive memory | Can run on consumer GPUs, CPUs, or NPUs |
| **Cost** | Millions of dollars per large model | Cents to dollars per use |
| **Frequency** | Done once (or periodically for updates) | Happens every time someone uses the model |

## The Compute Crisis

AI's hunger for compute is creating several challenges:

### Supply Constraints
- Data center GPUs are in extremely high demand — often backordered months ahead
- Building data centers requires massive infrastructure (power, cooling, networking)
- Geopolitical tensions restrict chip exports to certain countries

### Energy Costs
Training a single large model can consume as much electricity as hundreds of homes use in a year. The environmental impact is significant:
- Training GPT-3 estimated at ~1,287 MWh (enough for ~120 US homes annually)
- Inference (daily usage) consumes far more total energy than training over time

### Cost Barriers
The compute requirements create a barrier to entry:
- Training a frontier model costs $100M-$1B+
- Even running inference at scale requires millions in infrastructure
- This concentrates AI power in the hands of a few well-funded companies

## What Compute Is NOT

- **Not just about raw speed** — memory bandwidth, interconnect speed between GPUs, and software optimization matter as much as FLOPS (floating-point operations per second)
- **Not getting cheaper forever** — while individual chips improve, total compute needs grow faster than hardware improvements (Moore's Law isn't keeping up with AI demand)
- **Not only a GPU problem** — CPUs, NPUs, and specialized accelerators all play roles in the compute ecosystem

## Why It Matters

Compute is the fundamental resource that determines what AI is possible. The models we can train, how fast they improve, and who can afford to build them are all constrained by compute availability and cost. Understanding compute helps you:
- Choose the right hardware for your use case (local vs. cloud)
- Estimate costs for running or training models
- Understand why AI development is concentrated among a few organizations
- Make informed decisions about open vs. proprietary approaches

## Related Terms
- [Inference Cost](inference-cost.md) — how compute translates to pricing
- [Quantization](../tier2/quantization.md) — reducing compute requirements for running models
- [LLM (Large Language Model)](../tier2/llm.md) — what requires all this compute
