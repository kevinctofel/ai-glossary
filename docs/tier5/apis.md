# AI APIs (Application Programming Interfaces)

**AI APIs** are interfaces that let software applications interact with AI models over the internet. Instead of running an AI model on your own computer, you send requests to a server that runs the model and returns responses — like calling a phone number instead of building your own telephone system.

## The Simple Version

Think of an API as a restaurant kitchen:
- You (the app) are the customer placing an order through the waiter (the API)
- The kitchen (the AI model server) prepares the food (generates the response)
- The waiter brings it back to you

You don't need to know how the kitchen works, what ingredients they use, or how many chefs are cooking. You just send your request and get a result. This is why APIs make AI accessible — you don't need GPUs, massive storage, or ML expertise to use powerful models.

## How AI APIs Work

### The Basic Flow
1. **You send a request** — typically JSON containing your prompt, model name, and parameters (temperature, max tokens, etc.)
2. **The API server processes it** — sends the prompt to the model, runs inference
3. **You get a response** — the generated text, plus metadata (tokens used, processing time)

### Common API Parameters

| Parameter | What It Controls | Typical Values |
|-----------|-----------------|---------------|
| `model` | Which AI model to use | gpt-4o, claude-sonnet-4, etc. |
| `messages` | The conversation/prompt | Array of role + content objects |
| `temperature` | Creativity vs. determinism ([Temperature](../tier1/temperature-sampling.md)) | 0.0 (strict) to 1.0 (creative) |
| `max_tokens` | Maximum response length | 256, 1024, 4096 |
| `top_p` | Alternative to temperature for controlling randomness | 0.1 to 1.0 |

## Types of AI APIs

### Completion/Chat APIs
The most common type — send text, get text back:
```json
POST /v1/chat/completions
{
  "model": "gpt-4o",
  "messages": [{"role": "user", "content": "Explain quantum computing"}]
}
```

### Function Calling APIs
Let the model decide which tools to use:
```json
{
  "functions": [
    {"name": "get_weather", "description": "Get current weather for a location"},
    {"name": "calculate", "description": "Perform a math calculation"}
  ]
}
```

### Embedding APIs
Convert text to numerical vectors ([Embeddings](../tier3/embeddings.md)):
```json
POST /v1/embeddings
{
  "model": "text-embedding-3-small",
  "input": ["What is AI?", "How does ML work?"]
}
```

### Image Generation APIs
Generate images from text descriptions ([Image & Video Generation](../tier3/image-video-generation.md)):
```json
POST /v1/images/generations
{
  "model": "dall-e-3",
  "prompt": "A sunset over mountains in watercolor style"
}
```

## Pricing Models

| Model | How It Works | Example Cost |
|-------|-------------|-------------|
| **Per-token** | Charge based on input + output tokens | ~$0.01 per 1K tokens (input), ~$0.03 per 1K tokens (output) |
| **Per-request** | Fixed price per API call regardless of length | $0.05-$2.00 per request depending on model tier |
| **Subscription** | Monthly fee for a set number of requests/credits | $20/month for 100K requests, $200/month for 1M |
| **Enterprise** | Custom pricing based on volume and SLA requirements | Negotiated rates for high-volume users |

## What AI APIs Are NOT

- **Not free** — even "free tiers" have limits. Running AI models costs real money (compute, electricity, hardware)
- **Not instant** — response time depends on model complexity, server load, and response length (typically 0.5-5 seconds)
- **Not perfectly reliable** — APIs can rate-limit, timeout, or return errors. Good apps handle failures gracefully
- **Not a substitute for understanding the model** — knowing how LLMs work ([LLM](../tier2/llm.md)) helps you use APIs effectively

## API Best Practices

1. **Cache responses** — identical prompts don't need to hit the API every time
2. **Handle errors** — implement retry logic and graceful degradation
3. **Monitor token usage** — costs add up quickly; track spending
4. **Use streaming** — for long responses, stream tokens as they're generated instead of waiting for the full response
5. **Validate inputs** — sanitize prompts to prevent injection attacks or unexpected behavior

## Why It Matters

AI APIs democratized access to powerful models. You don't need a data center or ML team to build AI-powered applications — just an API key and some code. This has enabled thousands of startups, indie developers, and enterprises to integrate AI into their products. Understanding APIs is essential for anyone building with AI today.

## Related Terms
- [LLM (Large Language Model)](../tier2/llm.md) — what the APIs provide access to
- [Compute](compute.md) — what powers API servers behind the scenes
- [Inference Cost](inference-cost.md) — how API pricing relates to compute costs
