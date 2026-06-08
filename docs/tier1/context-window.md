# Context Window

**Context window** is the maximum amount of text (measured in tokens) that an AI model can process at one time — both what you give it and what it generates in response.

## The Simple Version

Imagine a notepad with limited space. You write your question on it, and the AI reads everything on the notepad to form its answer. Once the notepad is full, it can't read anything more. That limit is the context window.

## How It Works

When you send a message to an AI:
1. Your message gets converted to tokens
2. Any previous messages in the conversation also get converted to tokens
3. All those tokens together must fit within the model's context window
4. The model reads everything and generates a response (which also uses tokens)

## Common Context Window Sizes

| Model | Typical Context Window | What It Means |
|-------|----------------------|---------------|
| Older models | 2,000–4,000 tokens | ~1,500–3,000 words (a short email) |
| Modern models | 8,000–32,000 tokens | ~6,000–24,000 words (a long article or book chapter) |
| Latest models | 100,000–1,000,000+ tokens | ~75,000–750,000 words (multiple books) |

## Why Context Window Matters

### For Conversations
In a long chat, every message you send and every response the AI gives counts toward the context window. After many back-and-forths, you might hit the limit and the model will "forget" the beginning of the conversation.

### For Documents
If you paste a 50-page document into an AI with an 8K context window, it can only process roughly the first 16 pages. The rest gets cut off.

### For Cost
More tokens in your context window = more compute = higher cost for the service provider (and often higher price for you).

## What Happens When You Hit the Limit?

Different systems handle this differently:
- **Hard cutoff** — anything beyond the limit is ignored completely
- **Sliding window** — the oldest messages get dropped to make room for new ones
- **Summarization** — some systems summarize earlier parts of the conversation to save space

## Tips for Managing Context Window

1. **Be concise** in your prompts — fewer tokens means more room for the AI's response
2. **Start fresh conversations** for unrelated topics — old messages eat up context
3. **Paste documents strategically** — if you need analysis of a long document, ask specific questions about sections rather than dumping everything at once
4. **Check the model specs** — before pasting large files, look up the model's context window limit

## Related Terms
- [Tokens & Tokenization](tokens-tokenization.md) — what gets counted toward your context window
- [Prompts & Prompt Engineering](prompts.md) — how to structure input efficiently
- [Inference vs. Training](inference-vs-training.md) — context window matters during inference (when the model is actually responding)
