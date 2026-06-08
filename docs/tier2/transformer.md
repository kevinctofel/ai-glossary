# Transformer

**The Transformer** is a neural network architecture introduced in a 2017 paper called "Attention Is All You Need." It's the foundational design that made modern large language models possible — every major LLM today (GPT, Claude, Gemini, etc.) uses some variant of Transformers.

## The Simple Version

Before Transformers, AI systems processed information one step at a time, like reading a sentence word by word and remembering each word as they went. This was slow and struggled with long texts because the model could "forget" earlier parts.

Transformers changed everything by letting the model look at **all** the words in a text simultaneously and figure out which words are most relevant to each other — like reading an entire paragraph at once and instantly seeing how different ideas connect. This is called "attention."

## How Attention Works

Imagine you're reading this sentence: *"The cat, which had been sleeping on the sofa all afternoon, finally jumped onto the table."*

A Transformer's attention mechanism asks: when I see the word "cat," what other words should I pay extra attention to? It might highlight "sofa" (where it was), "afternoon" (when), and "jumped" (what it did). This lets the model understand relationships between distant parts of text that earlier systems would miss.

## Key Components

### Self-Attention
Each word in your input looks at every other word and assigns a relevance score. Words that are semantically related get higher scores, helping the model build a rich understanding of context.

### Multi-Head Attention
Instead of one attention mechanism, Transformers use multiple "heads" — each head learns different types of relationships (grammar, semantics, temporal order, etc.). Think of it as having several people reading the same text and each noticing different patterns.

### Position Encoding
Since Transformers process all words at once (not sequentially), they need a way to know word order. Position encoding adds information about where each word appears in the sequence.

## Why Transformers Changed Everything

| Before Transformers | With Transformers |
|--------------------|-------------------|
| Processed text sequentially (slow) | Processes all tokens in parallel (fast) |
| Struggled with long-range dependencies | Handles relationships across entire documents |
| Required specialized architectures for each task | One architecture works for language, vision, audio |
| Hard to scale | Scales beautifully — bigger models = better performance |

## What Transformers Are NOT

- **Not a model themselves** — they're an architecture (a blueprint). LLMs like GPT are *built using* Transformer architectures
- **Not always the best choice** — for some tasks (like processing very long videos or certain types of time-series data), other architectures may be more efficient
- **Not magic** — despite their power, they still have fundamental limitations around reasoning and true understanding

## Why It Matters

Understanding Transformers helps you understand why modern AI works the way it does. The attention mechanism is what gives LLMs their ability to maintain context, follow instructions across long conversations, and connect ideas that seem unrelated on the surface. Every breakthrough in AI since 2017 has built on this architecture.

## Related Terms
- [LLM (Large Language Model)](llm.md) — models built using Transformer architecture
- [Deep Learning](../tier1/deep-learning.md) — the broader approach Transformers fall under
- [Parameters](../tier1/parameters.md) — what gets learned during training of a Transformer
- [Context Window](../tier1/context-window.md) — how much text a Transformer can process at once
