# AI Agents

**An AI Agent** is a system that uses an AI model not just to generate text, but to take actions — making decisions, using tools, interacting with other systems, and working toward a goal over multiple steps. Think of it as the difference between asking someone for directions (LLM) versus asking them to plan a trip, book flights, and navigate there (Agent).

## The Simple Version

A regular LLM is like a knowledgeable consultant: you ask a question, it gives an answer, and that's the end of the interaction. An AI agent is more like an assistant: you give it a goal ("Plan a vacation to Japan for under $3000"), and it figures out what steps to take, uses tools (search, calculators, booking APIs) to gather information, makes decisions along the way, and keeps working until the goal is complete.

## How Agents Work

### The Core Loop
Agents operate in a repeated cycle:

1. **Observe** — Look at the current state (what's been done so far, what tools are available)
2. **Think** — Use the LLM to decide what to do next based on the goal and current situation
3. **Act** — Execute an action (call a tool, send a message, make a calculation)
4. **Repeat** — Observe the results of the action and decide the next step

This loop continues until the agent reaches its goal or determines it can't proceed further.

### Tools
Agents use "tools" — functions they can call to interact with the outside world:
- Search the web
- Run code
- Read/write files
- Call APIs (weather, maps, databases)
- Send emails or messages
- Control other software

The LLM decides which tool to use and what parameters to pass, then interprets the results.

## Types of Agents

| Type | Description | Example |
|------|-------------|---------|
| **ReAct** | Reason + Act in alternating steps — the most common pattern | "I need weather data → call weather API → analyze results → decide next step" |
| **Planning agents** | Create a plan first, then execute it step by step | "To build this app: 1. Design UI 2. Write backend 3. Test" |
| **Multi-agent systems** | Multiple agents collaborate, each with specialized roles | One agent researches, one writes code, one reviews quality |
| **Autonomous agents** | Operate with minimal human intervention over extended periods | Monitor a system and fix issues when they arise |

## What AI Agents Are NOT

- **Not just chatbots with buttons** — adding a "search" button to a chat interface doesn't make it an agent. True agents reason about *when* and *how* to use tools
- **Not fully autonomous (yet)** — current agents still need human oversight, clear goal definitions, and guardrails against harmful actions
- **Not guaranteed to succeed** — agents can get stuck in loops, make wrong tool choices, or fail when goals are ambiguous

## Challenges with Agents

| Challenge | Why It's Hard |
|-----------|--------------|
| **Reliability** | LLMs aren't perfectly deterministic; an agent might take different paths each run |
| **Error handling** | When a tool call fails or returns unexpected data, the agent needs to recover gracefully |
| **Cost** | Each reasoning step consumes tokens — complex agents can be expensive to run |
| **Safety** | An agent with tool access could potentially do unintended things if goals aren't well-specified |
| **Debugging** | Multi-step agents are harder to debug than single-response LLMs because failures can happen at any step |

## Why It Matters

Agents represent the next evolution of AI from passive tools to active helpers. Instead of you doing all the work and asking AI for help along the way, you give AI a goal and it does the work — making decisions, using tools, and adapting as it goes. This is what turns AI from a fancy search engine into something that can actually *do* things for you.

## Related Terms
- [LLM (Large Language Model)](llm.md) — the "brain" that powers agents
- [RAG](rag.md) — often used by agents to access external information
- [Fine-tuning](fine-tuning.md) — can be used to improve agent behavior
- [Prompts & Prompt Engineering](../tier1/prompts.md) — goal specification is critical for agents
