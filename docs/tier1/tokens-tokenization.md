# Tokens & Tokenization

**Tokens** are the basic units of text that AI models read and write. **Tokenization** is the process of breaking text into these tokens.

## The Simple Version

AI doesn't read words the way you do. It chops text into smaller pieces called "tokens" — which can be whole words, parts of words, or even individual characters. Think of it like how a word processor might split text for processing, but done in a way optimized for machine learning.

## What Counts as a Token?

| Text | Tokens | Count |
|------|--------|-------|
| "Hello world" | ["Hello", "world"] | 2 tokens |
| "Unbelievable" | ["Un", "believe", "able"] | 3 tokens |
| "I'm going to the store." | ["I", "'", "m", "going", "to", "the", "store", "."] | 8 tokens |
| "The cat sat on the mat" | ["The", "cat", "sat", "on", "the", "mat"] | 6 tokens |

Notice how "Unbelievable" gets split into three pieces? That's because the model learned that "un-", "-believe", and "-able" are useful building blocks. Common words stay as single tokens; rare or complex words get chopped up.

## Why Tokens Matter (For You)

### 1. Cost
Most AI services charge **per token**. If your message gets split into more tokens, it costs more. Understanding tokenization helps you write efficiently.

### 2. Context Window
Every model has a maximum number of tokens it can process at once (the "context window"). Knowing how tokenization works helps you understand why your long document might get cut off.

### 3. Language Differences
Tokenization works differently across languages:
- **English** — words are separated by spaces, so tokenization is relatively straightforward
- **Chinese/Japanese** — no spaces between words, so tokenization has to figure out word boundaries (more complex)
- **German/Dutch** — compound words can create very long tokens that get split

## What Tokenization Is NOT

- **Not the same as character counting** — "Hello" is 5 characters but usually just 1 token
- **Not consistent across models** — different AI companies use different tokenizers, so the same text might produce different token counts in different systems
- **Not perfect** — sometimes tokenization splits words awkwardly or merges things it shouldn't

## Quick Tips for Working with AI

- Be concise — fewer tokens = cheaper and faster
- Avoid unnecessary repetition — each word costs a token
- If you're pasting long documents, be aware that they'll consume your context window quickly
- Special characters and punctuation count as tokens too

## Related Terms
- [Context Window](context-window.md) — how many tokens a model can handle at once
- [Prompts & Prompt Engineering](prompts.md) — how you structure input for AI
- [Parameters](parameters.md) — what the model learns during training
