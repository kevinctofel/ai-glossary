# Fine-Tuning

**Fine-tuning** is the process of taking a pre-trained AI model and training it further on a specific dataset to specialize it for a particular task or domain. It's like giving a generalist doctor additional training in cardiology — they already know medicine, but now they're better at heart-related problems.

## The Simple Version

When an LLM is first trained (pre-training), it learns from billions of pages of diverse text — books, articles, code, forums, everything. It becomes good at a lot of things but isn't great at anything specific. Fine-tuning takes that general model and teaches it to excel at something narrower: answering medical questions, writing legal documents, coding in Python, or chatting in a particular style.

## How It Works

### Step 1: Start with a Pre-trained Model
You begin with an existing model (like Llama, Mistral, or Qwen) that already understands language broadly. You don't train from scratch — you build on what's already there.

### Step 2: Prepare Your Dataset
Create a dataset of examples specific to your task. For example:
- **Customer service bot:** Thousands of customer questions with ideal responses
- **Code assistant:** Code snippets paired with explanations
- **Medical Q&A:** Medical questions with expert answers

The quality and quantity of this dataset matters enormously — fine-tuning on bad data makes a good model worse.

### Step 3: Train (Fine-Tune)
Run the pre-trained model on your dataset, adjusting its parameters slightly to optimize for your specific task. This is much cheaper than training from scratch because most of the knowledge is already there.

### Step 4: Evaluate and Iterate
Test the fine-tuned model on new examples. If it's not performing well enough, adjust the dataset or training parameters and try again.

## Fine-Tuning vs. Pre-training

| Aspect | Pre-training | Fine-tuning |
|--------|-------------|-------------|
| Data source | Massive, diverse internet text | Specific, curated dataset |
| Cost | Millions of dollars | Hundreds to thousands of dollars |
| Time | Months | Hours to days |
| Result | General-purpose model | Specialized model |
| Who does it | Big tech companies, research labs | Anyone with a good dataset and compute |

## Common Fine-Tuning Approaches

### Full Fine-tuning
Adjust all the model's parameters. Most effective but most expensive.

### Parameter-Efficient Fine-tuning (PEFT)
Only adjust a small subset of parameters while keeping most frozen. Techniques include:
- **LoRA** (Low-Rank Adaptation): Adds small trainable layers on top of the existing model — popular because it's cheap and effective
- **QLoRA**: LoRA with quantization ([Quantization](quantization.md)) for even lower resource requirements

### Instruction Fine-tuning
Train the model to follow instructions in a consistent format. This is what turns a raw language model into something that behaves like ChatGPT — it learns to respond helpfully to prompts rather than just continuing text.

## What Fine-Tuning Is NOT

- **Not a magic fix for bad data** — if your training examples are wrong, biased, or inconsistent, the fine-tuned model will be too
- **Not permanent** — models can drift from their original capabilities after aggressive fine-tuning (called "catastrophic forgetting")
- **Not always necessary** — sometimes [RAG](rag.md) (giving a model access to external data at inference time) is better than fine-tuning

## Why It Matters

Fine-tuning democratizes AI. You don't need billions of dollars or a data center to build a specialized AI system anymore. With the right dataset and some compute, you can adapt powerful open models to your specific needs — whether that's building a domain-specific chatbot, automating document processing, or creating a personalized writing assistant.

## Related Terms
- [LLM (Large Language Model)](llm.md) — what gets fine-tuned
- [RLHF](rlhf.md) — a type of fine-tuning using human feedback
- [RAG](rag.md) — an alternative to fine-tuning for adding domain knowledge
- [Quantization](quantization.md) — how to make fine-tuning cheaper
