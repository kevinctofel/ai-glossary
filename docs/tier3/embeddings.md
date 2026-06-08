# Embeddings

**Embeddings** are numerical representations of information — like words, images, or documents — that capture their meaning in a way computers can understand and compare. Think of them as converting concepts into coordinates on a map where similar things are close together.

## The Simple Version

Imagine you have a giant library and want to find books about "climate change." Instead of searching for the exact words "climate" and "change," an embedding system converts each book's content into a set of numbers that represent its *meaning*. Then it can find books about "global warming," "environmental impact," or "carbon emissions" — even if those exact words never appear — because their numerical representations are close to yours.

Embeddings turn words and concepts into points in a multi-dimensional space where distance equals similarity.

## How Embeddings Work

### From Text to Numbers
When an AI model processes text, it doesn't just see individual words — it converts them into vectors (lists of numbers). A typical embedding might be 384, 768, or even 1536 numbers long. Each number captures some aspect of the word's meaning:

- Word "king" might have high values in dimensions related to royalty, leadership
- Word "queen" would be very similar but slightly different (same dimensions, different values)
- Word "apple" would be far away from both (different semantic territory)

### The Semantic Map
If you plotted these vectors visually:
```
                    Leadership
                        ↑
           King ←──────┼──────→ Queen
                        |
                        |
           Man ←────────┼────────→ Woman
                        |
                        ↓
                   Royalty
```

Words with similar meanings cluster together. "King" is close to "queen," "monarch," and "throne." "Apple" clusters near "fruit," "orange," and "banana." This spatial relationship is what makes embeddings powerful for search, classification, and recommendation.

## What Embeddings Are Used For

| Application | How Embeddings Help |
|------------|-------------------|
| **Semantic search** | Find documents by meaning, not just keywords ([RAG](../tier2/rag.md)) |
| **Recommendation systems** | "People who liked X also liked Y" based on similarity |
| **Duplicate detection** | Identify near-duplicate content even with different wording |
| **Clustering** | Group similar items automatically (customer segments, topic categories) |
| **Anomaly detection** | Find outliers — items that are far from their expected cluster |

## Embedding vs. Tokenization

| Aspect | Tokenization ([Tokens](../tier1/tokens-tokenization.md)) | Embeddings |
|--------|-----------------------------------------------------|-----------|
| Purpose | Breaks text into processable units | Captures meaning of those units |
| Output | Discrete IDs (e.g., word "cat" = ID 4827) | Continuous numbers (e.g., [0.23, -1.45, 0.89...]) |
| Analogy | Like breaking a sentence into words | Like converting words to coordinates on a meaning-map |
| Used by | All LLMs internally | Search systems, recommendation engines, RAG pipelines |

## Common Embedding Models

| Model | Dimensions | Strengths |
|-------|-----------|-----------|
| **text-embedding-3-small** (OpenAI) | 1536 | Good general-purpose embeddings, widely used |
| **text-embedding-3-large** (OpenAI) | 3072 | Higher quality but more expensive/computationally heavy |
| **sentence-transformers/all-MiniLM-L6-v2** | 384 | Open source, fast, runs locally, surprisingly effective |
| **BGE (BAAI General Embedding)** | 768+ | Strong multilingual support, open source |

## What Embeddings Are NOT

- **Not a database** — embeddings are just numbers. You need a vector database or search system to store and query them efficiently
- **Not perfectly accurate** — similarity in embedding space doesn't always match human judgment of relevance
- **Not reversible** — you can't convert an embedding back into the original text (it's a one-way transformation)
- **Not magic similarity** — two embeddings being "close" means they're semantically similar in the model's training, not necessarily in your specific use case

## Challenges

| Challenge | Description |
|-----------|-------------|
| **Dimensionality** | High-dimensional spaces (384+ dimensions) are hard to visualize and reason about |
| **Bias** | Embeddings inherit biases from their training data — similar concepts may cluster differently across cultures |
| **Domain mismatch** | General embeddings may not work well for specialized fields (medical, legal, technical) |
| **Storage at scale** | Storing and searching billions of embeddings requires specialized infrastructure |

## Why It Matters

Embeddings are the invisible glue holding together much of modern AI's ability to understand and organize information. They power search engines that find what you mean rather than just matching keywords, recommendation systems that suggest relevant content, and RAG pipelines that connect LLMs to external knowledge. Understanding embeddings helps you understand how AI "understands" meaning — not by knowing definitions, but by mapping concepts into a space where similarity has mathematical meaning.

## Related Terms
- [RAG](../tier2/rag.md) — uses embeddings for document retrieval
- [Tokens & Tokenization](../tier1/tokens-tokenization.md) — embeddings build on tokenized text
- [LLM (Large Language Model)](../tier2/llm.md) — LLMs generate embeddings as part of their internal processing
