# Chatbots

**Chatbots** are AI systems designed to have conversations with humans through text (or voice). Modern chatbots powered by LLMs ([LLM](../tier2/llm.md)) can understand context, remember previous messages in a conversation, and generate natural-sounding responses — making them far more useful than the rigid, rule-based bots of the past.

## The Simple Version

Old chatbots worked like phone menus: "Press 1 for sales, press 2 for support." They could only handle very specific, pre-programmed inputs. If you said something unexpected, they'd give up or loop endlessly.

Modern AI chatbots are more like talking to a knowledgeable person. You can ask questions in your own words, change topics mid-conversation, and get nuanced answers. The difference is that instead of following hardcoded rules, the chatbot uses an LLM to understand what you mean and generate appropriate responses.

## How Modern Chatbots Work

### Conversation Memory
Chatbots maintain context by keeping track of the conversation history. Each new message is sent along with previous messages so the model understands what you're referring to. This is limited by the [Context Window](../tier1/context-window.md) — if a conversation gets too long, earlier messages may be dropped.

### System Prompts
Behind every chatbot is a "system prompt" — hidden instructions that define its personality, rules, and capabilities:
- *"You are a helpful customer service assistant for Acme Corp."*
- *"You are a coding tutor who explains concepts step by step."*
- *"You are a creative writing partner who gives constructive feedback."*

The system prompt shapes how the chatbot behaves without you having to specify it every time.

### Tool Integration
Advanced chatbots can use tools ([AI Agents](../tier2/agents.md)) to go beyond text:
- Look up real-time information (weather, stock prices)
- Access databases or APIs
- Perform calculations
- Execute code
- Control other applications

## Chatbot Use Cases

| Domain | Example | Value |
|--------|---------|-------|
| **Customer service** | Answering product questions, processing returns | 24/7 support at fraction of human cost |
| **Education** | Tutoring students, explaining concepts at their level | Personalized learning available anytime |
| **Healthcare** | Symptom checking, medication info, mental health support | Accessible preliminary guidance (not diagnosis) |
| **Sales** | Qualifying leads, product recommendations | Always-available sales assistant |
| **Internal tools** | Helping employees find company information | Reduces time spent searching documentation |

## What Chatbots Are NOT

- **Not human replacements** — they handle routine interactions well but struggle with complex emotional situations or highly nuanced judgment calls
- **Not always accurate** — chatbots can confidently give wrong answers ([Hallucination](../tier4/hallucination.md)), especially on topics outside their training data
- **Not private by default** — conversations may be logged, used for training, or accessible to the service provider. Check privacy policies carefully

## Limitations to Watch For

| Issue | What It Looks Like | How to Mitigate |
|-------|-------------------|-----------------|
| **Context loss** | Forgets what you said earlier in long conversations | Keep conversations focused; summarize periodically |
| **Over-confidence** | States uncertain information as fact | Ask for sources or confidence levels |
| **Persona drift** | Loses its defined personality over long chats | Reset conversation or restate system instructions |
| **Jailbreaking** | Users finding ways to bypass safety restrictions | Important for developers building public-facing bots |

## Why It Matters

Chatbots are the most visible and widely-used AI application. They're in your phone (Siri, Google Assistant), on websites (customer support), in productivity tools (Copilot), and increasingly embedded in everyday services. Understanding how they work helps you use them effectively — knowing when to trust their answers, when to ask for clarification, and what limitations to expect.

## Related Terms
- [LLM (Large Language Model)](../tier2/llm.md) — the technology powering modern chatbots
- [AI Agents](../tier2/agents.md) — chatbots that can take actions beyond text
- [RAG](../tier2/rag.md) — giving chatbots access to specific knowledge bases
- [Prompts & Prompt Engineering](../tier1/prompts.md) — system prompts define bot behavior
