# Machine Learning

**Machine Learning (ML)** is a subset of AI where computers learn patterns from data instead of being explicitly programmed with rules for every situation.

## The Simple Version

Traditional programming: You write instructions like "if the email contains 'winner' and 'Nigeria', mark as spam."

Machine learning: You show the computer 10,000 emails labeled "spam" or "not spam," and it figures out which words and patterns indicate spam on its own.

## How It Works (Three Steps)

### 1. Training
You feed the system lots of examples with known answers. For a spam filter, that's thousands of emails already marked as spam or not-spam. The system adjusts its internal settings to match the patterns it sees.

### 2. Validation
You test the system on new data it hasn't seen before. If it correctly identifies 95% of test emails as spam/not-spam, you know it's learned something useful.

### 3. Prediction
The trained system processes new, unseen data and makes guesses based on what it learned during training.

## Common Types of Machine Learning

| Type | How It Works | Example |
|------|-------------|---------|
| **Supervised** | Learns from labeled examples (like a student with answer keys) | Email spam detection, image classification |
| **Unsupervised** | Finds patterns in unlabeled data (like exploring without a map) | Customer segmentation, anomaly detection |
| **Reinforcement** | Learns by trial and error, getting rewards/punishments | Game-playing AI, robot navigation |

## What Machine Learning Is NOT

- **Not the same as AI** — ML is one approach to building AI. Other approaches include rule-based systems that don't "learn" at all
- **Not guaranteed accuracy** — garbage data in = garbage results out ("garbage in, garbage out")
- **Not a black box you can ignore** — understanding what data was used to train a model is crucial for knowing when it might fail

## Why It Matters

Machine learning powers most of the AI features people interact with daily: recommendation systems, voice assistants, fraud detection, and yes, the large language models that generate text. If you understand ML, you understand how most modern AI actually works under the hood.

## Related Terms
- [What is AI?](what-is-ai.md) — the broader field
- [Deep Learning](deep-learning.md) — a powerful type of machine learning using neural networks
- [Parameters](parameters.md) — what the system "learns" during training
- [RLHF](../tier2/rlhf.md) — how AI gets trained to be helpful and safe
