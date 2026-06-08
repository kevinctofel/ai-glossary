# RAG (Retrieval-Augmented Generation)

**RAG** stands for **Retrieval-Augmented Generation**. It's a technique that gives AI models access to external information at the time they generate a response, rather than relying solely on what they learned during training. Think of it as letting the model look up references while writing an essay instead of just using its memory.

## The Simple Version

A regular LLM answers questions based only on what it memorized during training — like taking a test from memory with no notes allowed. RAG changes that by giving the model access to a knowledge base (documents, databases, websites) right when you ask a question. It first retrieves relevant information, then uses that information to generate its answer.

## How It Works (Two Steps)

### Step 1: Retrieval
When you ask a question, the system searches through a collection of documents to find the most relevant ones. This is done using **embeddings** ([Embeddings](../tier3/embeddings.md)) — numerical representations of text that capture meaning. Documents with similar meanings to your query get ranked higher and pulled into context.

### Step 2: Generation
The retrieved documents are fed to the LLM along with your original question. The model reads them and generates an answer based on both its general knowledge and the specific information it just retrieved. This is "augmented generation" — the model's output is enhanced by external data.

## Why RAG Is Powerful

| Problem | Without RAG | With RAG |
|---------|------------|----------|
| Outdated knowledge | Model only knows what it was trained on (could be months/years old) | Always has access to current information |
| Domain-specific expertise | General models lack deep knowledge in narrow fields | Can be connected to specialized databases |
| Verifiability | Hard to know where the model's answer came from | Answers are grounded in specific documents you can check |
| Privacy/security | Training data may contain sensitive info | Sensitive docs stay in your own database, not in model weights |

## Common RAG Use Cases

- **Customer support bots** — connected to your product documentation and FAQ
- **Research assistants** — searching through academic papers or internal reports
- **Legal analysis** — retrieving relevant case law and statutes
- **Enterprise knowledge search** — letting employees find information across company documents
- **Fact-checking** — grounding AI responses in verified sources

## What RAG Is NOT

- **Not a replacement for fine-tuning** — RAG adds external knowledge; fine-tuning changes the model's behavior. They're often used together
- **Not perfect retrieval** — if the retrieval step misses relevant documents, the generation step can't help. Garbage in (retrieval) = garbage out (answer)
- **Not just "Google for AI"** — it's more sophisticated than keyword search because embeddings capture semantic meaning, not exact word matches

## Challenges with RAG

| Challenge | Description |
|-----------|-------------|
| **Chunking** | How to split documents into pieces for retrieval. Too small = missing context; too large = noisy results |
| **Hallucination risk** | Models can still make things up even when given source documents, especially if the retrieved info is ambiguous |
| **Latency** | Retrieval adds a step before generation, making responses slower than plain LLM queries |
| **Scalability** | Searching through millions of documents efficiently requires good indexing and embedding infrastructure |

## Why It Matters

RAG is one of the most practical ways to make AI useful in real-world applications. It solves the biggest limitation of standalone LLMs — stale, unverifiable knowledge — by connecting them to fresh, specific information sources. If you're building an AI application for a business or organization, RAG is likely the first technique you'll implement.

## Related Terms
- [LLM (Large Language Model)](llm.md) — what generates the answers in RAG
- [Embeddings](../tier3/embeddings.md) — how retrieval finds relevant documents
- [Fine-tuning](fine-tuning.md) — often combined with RAG for best results
- [Context Window](../tier1/context-window.md) — limits how much retrieved info can be fed to the model
