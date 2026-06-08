# Inference vs. Training

**Training** is when an AI model learns from data. **Inference** (or "running" the model) is when it uses what it learned to answer questions or perform tasks.

## The Simple Version

Think of a student:
- **Training** = going to school, studying textbooks, doing practice problems for months or years
- **Inference** = taking a test, using everything you've learned to give an answer right now

You train a model once (expensive, takes time). You run it many times (cheaper, happens in real-time).

## Training: The Expensive Part

During training:
1. The model is fed massive amounts of data (books, websites, code, images)
2. It adjusts billions of internal settings (called "parameters") to find patterns
3. This takes days or weeks on specialized hardware (GPUs/TPUs)
4. It costs thousands to millions of dollars in compute

Training happens **once** (or occasionally re-trained with new data). The result is a trained model file that can be shared and used by anyone.

## Inference: The Everyday Part

During inference:
1. You send a prompt to the trained model
2. The model processes your input using what it learned during training
3. It generates a response in seconds (or milliseconds)
4. This happens **every time** someone uses the AI

Inference is what you experience when chatting with an AI, asking for a summary, or generating text. It's faster and cheaper than training, but it still requires compute resources.

## Key Differences

| | Training | Inference |
|--|---------|-----------|
| **When** | Once (or periodically) | Every time someone uses the model |
| **Duration** | Days to weeks | Seconds to milliseconds |
| **Cost** | Very high ($10K–$10M+) | Relatively low (cents per request) |
| **Hardware** | Massive GPU clusters | Single GPUs or even CPUs for small models |
| **Data needed** | Billions of examples | Just your prompt |
| **Who does it** | AI companies, research labs | Anyone with access to the model |

## Why This Distinction Matters

### For Cost
When you pay for an AI service, most of that cost goes toward inference (running the model for each request). Training costs are sunk — already paid by the company that built the model.

### For Privacy
Your prompts go through inference, not training. Reputable services don't use your conversations to retrain their models (though you should always check the terms of service).

### For Self-Hosting
You can download a trained model and run it yourself (self-hosted inference). You can't "train" a model on your laptop — that requires massive resources. But inference is something many people can do locally with the right hardware.

### For Model Updates
When a company releases a "new version" of their AI, they usually did more training (or fine-tuning) to create an improved model. The old trained model doesn't change — it's replaced by a new one.

## Related Terms
- [Parameters](parameters.md) — what gets adjusted during training
- [Fine-Tuning](tier2/fine-tuning.md) — a cheaper form of re-training on specific data
- [Context Window](context-window.md) — matters during inference (how much you can send at once)
