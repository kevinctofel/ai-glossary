# Open Source vs. Proprietary AI

**Open source vs. proprietary AI** describes the fundamental divide between AI models whose weights and training methods are publicly available (open source) versus those kept secret by companies (proprietary). This isn't just about access — it shapes who controls AI technology, how safe it is, and where innovation happens.

## The Simple Version

Think of it like recipes:
- **Open source** = the full recipe is published. Anyone can cook it, modify it, improve it, or run it on their own stove
- **Proprietary** = the recipe is a secret. You can only eat the food at the restaurant (use the API), and you can't make it yourself or change how it's prepared

Both approaches have real trade-offs. Open source gives freedom and transparency; proprietary often delivers higher quality and easier access.

## Open Source AI

### What "Open" Means
A truly open AI model typically provides:
- **Model weights** — the actual trained parameters (the "knowledge")
- **Training code** — how the model was built
- **Training data details** — what the model learned from
- **Evaluation results** — independent testing of capabilities

### Popular Open Models

| Model | Developer | Size | Notable Feature |
|-------|-----------|------|----------------|
| **Llama** (Meta) | Meta/Facebook | 8B to 405B | Most widely adopted open model ecosystem |
| **Mistral** | Mistral AI (France) | 7B to 123B | Strong performance, European alternative |
| **Qwen** (Alibaba) | Alibaba | Various sizes | Strong multilingual capabilities |
| **Gemini Flash** (partial) | Google | Various | Some variants available with open weights |
| **DeepSeek** | DeepSeek (China) | Various | Cost-effective, strong reasoning |

### Advantages of Open Source

| Benefit | Why It Matters |
|---------|---------------|
| **Transparency** — anyone can inspect the model for bias, safety issues, or hidden behaviors | Independent auditing builds trust |
| **Privacy** — run models locally; your data never leaves your computer | No third-party data collection |
| **Customization** — fine-tune ([Fine-tuning](../tier2/fine-tuning.md)) for specific needs | Domain-specific applications without vendor lock-in |
| **Cost control** — no per-token API fees after initial compute investment | Predictable costs at scale |
| **Innovation** — anyone can build on top of the model | Faster ecosystem development |

### Limitations of Open Source

- **Quality gap** — proprietary models often outperform open ones (though the gap is narrowing rapidly)
- **Resource requirements** — running large models requires significant hardware (GPU, RAM)
- **Support** — no customer service or SLA guarantees; you're on your own for troubleshooting
- **Safety** — anyone can use open models for harmful purposes without access controls

## Proprietary AI

### What "Proprietary" Means
The model weights, training data, and methods are kept secret. Users interact through:
- **APIs** (send prompts, get responses)
- **Web interfaces** (chat websites like ChatGPT, Claude.ai)
- **Integrated products** (Copilot in VS Code, Gemini in Google Workspace)

### Popular Proprietary Models

| Model | Company | Access Method |
|-------|---------|--------------|
| **GPT-4/GPT-5** | OpenAI | API, ChatGPT web app |
| **Claude** (Anthropic) | Anthropic | API, Claude web app |
| **Gemini** | Google | API, Gemini web app, integrated products |
| **Copilot models** | Microsoft/OpenAI | Integrated into GitHub, VS Code, Office |

### Advantages of Proprietary

| Benefit | Why It Matters |
|---------|---------------|
| **Quality** — generally more capable than open alternatives | Better results for complex tasks |
| **Ease of use** — no setup required; just sign up and start | Accessible to non-technical users |
| **Support** — customer service, documentation, SLAs | Reliability for business use |
| **Safety controls** — built-in content filtering and usage monitoring | Reduced risk of misuse |
| **Continuous improvement** — companies invest heavily in R&D | Rapid capability advances |

### Limitations of Proprietary

- **No transparency** — you can't inspect how the model works or verify claims about its behavior
- **Vendor lock-in** — switching providers means retraining, rewriting integrations, and potentially losing capabilities
- **Data privacy concerns** — your prompts may be stored, reviewed, or used for training
- **Cost at scale** — API pricing can become expensive for high-volume applications
- **Censorship/control** — the provider decides what the model can and cannot discuss

## The Landscape Is Changing Fast

The gap between open and proprietary models has been closing rapidly:
- Open models now rival proprietary ones on many benchmarks
- Proprietary companies are releasing smaller open variants (Gemma from Google, Llama from Meta)
- Hybrid approaches emerge — base models open, fine-tuned versions proprietary
- Regulation may force more transparency regardless of open/closed status

## Why It Matters

The open vs. proprietary debate isn't just technical — it's about power and control:
- **Who decides** what AI can do and how it's used?
- **Who benefits** from AI improvements — everyone or just shareholders?
- **Who is safe** — centralized control (proprietary) or distributed oversight (open)?

For individuals, the choice depends on your needs: proprietary for ease and quality, open for privacy and control. For organizations, it's a strategic decision affecting security, cost, flexibility, and independence from tech giants.

## Related Terms
- [Fine-tuning](../tier2/fine-tuning.md) — open models enable custom fine-tuning; proprietary models generally don't
- [Privacy](privacy.md) — local open models offer stronger privacy than cloud APIs
- [Alignment](alignment.md) — open models allow independent alignment auditing
