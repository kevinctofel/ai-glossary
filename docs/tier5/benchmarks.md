# Benchmarks

**Benchmarks** are standardized tests used to measure and compare AI model performance. They provide a common language for discussing how capable different models are — like race times for athletes or test scores for students. However, benchmarks have significant limitations that anyone evaluating AI should understand.

## The Simple Version

Imagine trying to compare two students without knowing what they were tested on. One scored 95% on math but failed history; the other scored 80% across all subjects. Without context, you can't tell who's "better." Benchmarks try to solve this by creating standardized tests, but the test itself shapes what "good" looks like — and models can be optimized for the test without being genuinely better at everything.

## Common AI Benchmarks

### Language Understanding & Reasoning

| Benchmark | What It Tests | Description |
|-----------|--------------|-------------|
| **MMLU** (Massive Task Language Understanding) | General knowledge across 57 subjects | Multiple-choice questions spanning STEM, humanities, social sciences, law, and more. The industry standard for "general intelligence" |
| **GSM8K** | Math word problems | Grade-school level math problems requiring multi-step reasoning. Tests logical thinking, not just calculation |
| **HumanEval** | Code generation | Programming tasks where the model writes a function from its docstring. Evaluated by whether generated code passes test cases |
| **BIG-Bench Hard** | Complex reasoning | 204 tasks from the BIG-Bench suite, focusing on reasoning tasks that stumped earlier models |

### Conversational & Practical Ability

| Benchmark | What It Tests | Description |
|-----------|--------------|-------------|
| **MT-Bench** | Multi-turn conversation quality | Human evaluators rate model responses across multiple turns. Measures helpfulness, coherence, and instruction following |
| **Chatbot Arena** (LMSYS) | Head-to-head comparison | Users vote on which of two anonymous models gives a better response to their prompt. Crowd-sourced, real-world evaluation |
| **IFEval** (Instruction Following) | Prompt adherence | Tests whether models follow specific instructions precisely (format constraints, content requirements, negative constraints) |

### Specialized Domains

| Benchmark | What It Tests | Description |
|-----------|--------------|-------------|
| **MedQA** | Medical knowledge | Multiple-choice medical exam questions. Used to evaluate healthcare AI capabilities |
| **LegalBench** | Legal reasoning | Questions about legal concepts, case analysis, and statutory interpretation |
| **SWE-bench** | Software engineering | Real GitHub issues — can the model fix actual bugs in real codebases? |

## What Benchmarks Measure (and Don't Measure)

### What They're Good At
- Comparing models on specific, well-defined tasks
- Tracking progress over time within a benchmark
- Identifying relative strengths across different capability areas

### What They Miss
| Missing Aspect | Why It Matters |
|---------------|---------------|
| **Real-world performance** | A model scoring 90% on benchmarks may struggle with messy, ambiguous real prompts |
| **User satisfaction** | Benchmarks measure technical correctness, not whether humans find the output useful |
| **Safety and alignment** | High benchmark scores don't guarantee a model is safe or well-aligned ([Alignment](../tier4/alignment.md)) |
| **Context handling** | Most benchmarks test short prompts; real conversations involve long context windows ([Context Window](../tier1/context-window.md)) |
| **Tool use and agents** | Traditional benchmarks don't evaluate an AI's ability to use external tools ([AI Agents](../tier2/agents.md)) |

## The Benchmark Problem

### Over-Optimization (Gaming the Benchmarks)
As models improve on benchmarks, developers may inadvertently or intentionally optimize for those specific tests:
- Training data may include benchmark questions (data contamination)
- Models are fine-tuned specifically to perform well on popular benchmarks
- This creates an illusion of progress that doesn't translate to real-world capability

### The "Score Inflation" Issue
When everyone trains on the same benchmarks, scores become less meaningful:
- MMLU scores have risen dramatically, but partly because benchmark questions appear in training data
- A 90% score today may represent different actual ability than a 90% score did two years ago

### Why Chatbot Arena Matters
Crowd-sourced evaluations like Chatbot Arena (also called "LMSYS Chatbot Arena") address some benchmark limitations:
- Real users with real prompts, not curated test questions
- Blind A/B testing removes brand bias
- Results reflect actual user preferences, not abstract metrics

## How to Use Benchmarks Wisely

1. **Look at multiple benchmarks** — no single test captures overall capability
2. **Check the date** — older benchmark results may be outdated as models evolve
3. **Consider your use case** — a model that excels at math (GSM8K) may not be best for creative writing
4. **Trust real-world testing** — try the model with your actual prompts before relying on benchmark scores
5. **Beware of marketing numbers** — companies often highlight their best benchmark score while omitting weaker areas

## Why It Matters

Benchmarks are the closest thing we have to objective measures of AI capability, but they're imperfect tools. Understanding both what benchmarks can tell you and what they hide helps you make better decisions about which models to use, how to evaluate them for your needs, and when to trust (or question) published performance numbers.

## Related Terms
- [Model Cards](model-cards.md) — benchmarks are often reported in model documentation
- [LLM (Large Language Model)](../tier2/llm.md) — what's being benchmarked
- [Fine-tuning](../tier2/fine-tuning.md) — models can be optimized for specific benchmarks
