# Bias

**Bias** in AI refers to systematic errors or unfair preferences that cause an AI system to produce skewed, discriminatory, or inaccurate results. Unlike random mistakes (which cancel out over time), bias consistently pushes outputs in a particular direction — often reflecting prejudices present in the data the model was trained on.

## The Simple Version

Imagine a hiring tool that learned from 10 years of a company's past hires. If that company mostly hired men for technical roles, the AI would learn to associate "technical skill" with "male candidates" — not because it has opinions, but because its training data showed that pattern. It would then downgrade resumes from women applicants, even when they're equally qualified. The bias isn't intentional; it's baked into the patterns the model learned.

## Where AI Bias Comes From

### Training Data
AI models learn from vast amounts of text scraped from the internet, books, articles, and other sources. This data contains:
- Historical inequalities (past discrimination reflected in records)
- Cultural stereotypes (common assumptions about groups of people)
- Language patterns that favor certain dialects or writing styles
- Underrepresentation of minority perspectives

The model doesn't "believe" these things — it reproduces the statistical patterns it observed.

### Design Choices
Bias can also come from how systems are built:
- Which datasets were chosen for training (and which were excluded)
- How success is measured during evaluation (metrics that favor certain groups)
- Who participates in testing and review (homogeneous teams may miss biases)
- What safety filters are applied (which topics get restricted vs. allowed)

## Types of AI Bias

| Type | Description | Example |
|------|-------------|---------|
| **Representation bias** | Some groups are over- or under-represented in training data | Medical AI trained mostly on white patients performs worse on darker skin tones |
| **Association bias** | Model learns unfair correlations between attributes | "Nurse" associates more with female pronouns; "CEO" with male |
| **Measurement bias** | Evaluation metrics favor certain outcomes or groups | A language model scores higher on formal English than dialects like AAVE |
| **Deployment bias** | System is applied in contexts where it wasn't designed to work equally well | Facial recognition tested mostly on light-skinned faces fails on darker skin |

## How Bias Shows Up in LLMs

- **Stereotypical completions** — "The doctor said..." followed by male pronouns more often than female
- **Unequal treatment** — same prompt given to different demographic groups produces different quality responses
- **Toxicity asymmetry** — certain groups are flagged as "toxic" or "unsafe" more frequently for similar language
- **Cultural blind spots** — models perform worse on questions about cultures underrepresented in training data
- **Language hierarchy** — English and major languages get better treatment than minority languages

## Measuring and Reducing Bias

| Approach | How It Works | Limitations |
|----------|-------------|------------|
| **Bias benchmarks** | Standardized tests that measure bias across categories (gender, race, religion) | Can't capture all forms of bias; testing itself influences behavior |
| **Diverse training data** | Including more representative datasets from underrepresented groups | Hard to find quality data; may not address root causes |
| **Debiasing techniques** | Algorithmic methods to reduce biased associations during training | May degrade overall model performance; trade-offs are unclear |
| **Human review** | Diverse teams evaluate outputs for fairness issues | Subjective; hard to scale; reviewers bring their own biases |
| **Transparency** | Publishing training data sources, evaluation results, and known limitations | Doesn't fix bias but helps users understand it |

## What Bias Is NOT

- **Not intentional malice** — AI doesn't "hate" anyone. Bias is a statistical artifact, not a moral failing
- **Not unavoidable** — while some bias is inherent in any system trained on human data, it can be measured, reduced, and managed
- **Not just an "AI problem"** — humans have biases too; AI often amplifies them because it operates at scale and makes decisions consistently
- **Not fixed by saying 'be fair'** — telling a model to avoid bias in a prompt doesn't remove the underlying patterns in its training data

## Why It Matters

Bias in AI has real-world consequences. AI systems are increasingly used for hiring, lending, healthcare, criminal justice, education, and content moderation. When these systems carry bias, they can:
- Deny opportunities to qualified people
- Reinforce historical inequalities at scale
- Create feedback loops that make biases worse over time
- Erode trust in AI technology

Understanding bias helps you critically evaluate AI outputs, demand transparency from providers, and build systems that serve everyone fairly — not just the groups most represented in training data.

## Related Terms
- [Alignment](alignment.md) — ensuring AI serves human interests fairly
- [Hallucination](hallucination.md) — biased models may hallucinate more for underrepresented topics
- [Privacy](privacy.md) — bias and privacy concerns often overlap in data collection practices
- [Open Source vs. Proprietary](open-source-vs-proprietary.md) — open models allow independent bias auditing
