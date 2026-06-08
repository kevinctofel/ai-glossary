# LLM (Large Language Model)

**A Large Language Model (LLM)** is a type of AI trained on massive amounts of text to understand and generate human language. It's the technology behind chatbots like ChatGPT, Claude, Gemini, and models running locally on your computer.

## The Simple Version

Imagine reading every book, article, website, and forum post you could find — billions of pages of text. An LLM does something similar: it ingests enormous amounts of written content and learns the patterns of how humans use language. Then when you ask it a question or give it a task, it generates responses by predicting what words should come next based on everything it's learned.

## How It Works

### Training Phase
An LLM goes through two main training stages:

1. **Pre-training** — The model reads trillions of tokens (word fragments) from diverse sources and learns grammar, facts, reasoning patterns, and how different topics connect. This takes months and costs millions in compute.

2. **Fine-tuning** — After pre-training, the model is further trained on curated datasets to make it more helpful, accurate, and safe (see [RLHF](rlhf.md) for one approach).

### Inference Phase
When you interact with an LLM:
- Your prompt gets converted into tokens ([Tokens & Tokenization](../tier1/tokens-tokenization.md))
- The model processes those tokens through billions of parameters ([Parameters](../tier1/parameters.md))
- It generates a response one token at a time, using probability to pick the next word

## Key Characteristics

| Characteristic | What It Means | Why It Matters |
|---------------|-------------|----------------|
| **Scale** | Measured in billions or trillions of parameters | Larger models generally understand more complex tasks |
| **Context window** | How much text it can "remember" at once ([Context Window](../tier1/context-window.md)) | Determines how long a conversation or document it can handle |
| **Temperature** | Controls creativity vs. precision ([Temperature & Sampling](../tier1/temperature-sampling.md)) | Higher = more creative, lower = more factual/deterministic |
| **Open vs. closed** | Whether the model weights are publicly available | Open models let anyone run them locally; closed models require API access |

## What an LLM Is NOT

- **Not a search engine** — it generates responses from what it learned during training, not by looking up current information (unless connected to tools like [RAG](rag.md))
- **Not omniscient** — its knowledge is limited to what it was trained on and when that training ended
- **Not reasoning in the human sense** — it predicts text patterns, not "thinking" through problems with consciousness or understanding

## Why It Matters

LLMs are the foundation of most modern AI applications. They power chatbots, writing assistants, code generators, research tools, and increasingly autonomous systems. Understanding what LLMs can and can't do is essential for using them effectively and knowing when to trust their output.

## Related Terms
- [What is AI?](../tier1/what-is-ai.md) — the broader field
- [Transformer](transformer.md) — the architecture that makes modern LLMs possible
- [Fine-tuning](fine-tuning.md) — how models are specialized after pre-training
- [RLHF](rlhf.md) — training AI to be helpful and safe
- [RAG](rag.md) — giving LLMs access to external information
