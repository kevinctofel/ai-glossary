# Prompts & Prompt Engineering

A **prompt** is the input you give to an AI model — usually text, but sometimes images or other data. **Prompt engineering** is the practice of crafting those inputs to get better results.

## The Simple Version

Think of a prompt like giving instructions to a very smart but literal-minded assistant. The more clear, specific, and well-structured your instructions are, the better the result. But it's not just about being clear — it's about understanding *how* the AI processes information.

## What Makes Up a Prompt?

A typical prompt has these elements:
1. **The task** — what you want done ("Write a summary of...")
2. **Context** — background information the AI needs ("Here's an article about...")
3. **Format** — how you want the output structured ("Give me 5 bullet points")
4. **Constraints** — any limits or rules ("Keep it under 200 words, no jargon")

## Good Prompt Examples

### ❌ Weak Prompt
"Tell me about AI."

*Why it's weak:* Too broad. The AI could give you a paragraph, an essay, or a technical deep-dive. You have no idea what you'll get.

### ✅ Strong Prompt
"I'm a high school student writing a paper on artificial intelligence. Can you explain what AI is in 3-4 paragraphs? Use simple language and include one real-world example of how AI affects daily life."

*Why it's strong:* Specifies audience (high school), length (3-4 paragraphs), tone (simple language), and content requirement (real-world example).

## Prompt Engineering Techniques

### Chain of Thought
Ask the AI to explain its reasoning step by step before giving a final answer. This often produces more accurate results, especially for complex problems.

> "Think through this problem step by step, then give me your final answer."

### Few-Shot Learning
Give the AI examples of what you want before asking it to do the task.

> "Here are three examples of product descriptions I like: [examples]. Now write a description for our new coffee maker in the same style."

### Role Assignment
Tell the AI to adopt a specific perspective or expertise.

> "You're an experienced chef explaining this recipe to someone who's never cooked before."

### Structured Output
Ask for specific formats (JSON, tables, bullet points) when you need machine-readable results.

## What Prompt Engineering Is NOT

- **Not hacking or cheating** — it's just better communication with the system
- **Not guaranteed to work** — even perfect prompts can produce bad results if the model itself is limited
- **Not a one-size-fits-all** — different models respond differently to the same prompt structure

## Why It Matters

Prompt engineering is becoming an important skill because:
1. **Better results** — well-crafted prompts consistently produce higher quality output
2. **Cost savings** — clearer prompts mean fewer retries and less wasted tokens
3. **Reliability** — structured prompts reduce hallucinations and off-topic responses
4. **Accessibility** — good prompting lets non-technical users get great results from AI

## Quick Prompt Checklist

Before sending a prompt, ask yourself:
- [ ] Is my task clear and specific?
- [ ] Did I provide enough context?
- [ ] Did I specify the format I want?
- [ ] Are there any constraints I should mention (length, tone, audience)?
- [ ] Would giving an example help?

## Related Terms
- [Tokens & Tokenization](tokens-tokenization.md) — your prompt counts toward token limits
- [Context Window](context-window.md) — how much of your prompt the AI can actually read
- [Temperature & Sampling](temperature-sampling.md) — how creative vs. deterministic the response will be
