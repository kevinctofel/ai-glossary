# Deep Learning

**Deep Learning** is a type of machine learning that uses artificial neural networks with many layers (hence "deep") to learn increasingly abstract representations of data.

## The Simple Version

Imagine teaching someone to recognize cats:
- **Layer 1** notices edges and lines
- **Layer 2** combines those into shapes (circles, triangles)
- **Layer 3** puts shapes together into features (ears, whiskers, eyes)
- **Layer 4** recognizes the complete pattern as "cat"

Each layer builds on what the previous one found. That's deep learning — stacking layers of pattern recognition so the system can handle complex tasks like understanding language or seeing images.

## Where It Comes From

Deep learning is inspired by biological brains, but it's a very simplified analogy:
- **Neurons** in your brain fire when they detect certain patterns
- **Artificial neurons** do something similar — they activate when input matches what they've learned to recognize
- **Layers** of neurons process information step by step

The "deep" part just means there are many layers (sometimes hundreds), allowing the system to learn very complex patterns.

## What Deep Learning Is Good At

| Task | Example |
|------|---------|
| **Language** | Understanding and generating text, translation |
| **Images** | Recognizing objects, faces, medical scans |
| **Audio** | Speech recognition, music generation |
| **Video** | Action recognition, scene understanding |

## The Catch (What It Costs)

Deep learning is powerful but expensive:
- **Needs lots of data** — thousands or millions of examples to train properly
- **Needs lots of compute** — training can take days on specialized hardware (GPUs)
- **Needs lots of parameters** — modern models have billions of settings they learn during training
- **Hard to interpret** — it's often unclear *why* a deep learning model made a specific decision

## Deep Learning vs. Traditional Machine Learning

| | Traditional ML | Deep Learning |
|--|---------------|---------------|
| **Feature extraction** | You tell the computer what features matter (e.g., "look at word frequency") | The system figures out which features matter on its own |
| **Data needed** | Works with smaller datasets | Needs massive amounts of data |
| **Compute needed** | Can run on a laptop | Usually needs GPUs, sometimes clusters |
| **Performance** | Good for structured data (spreadsheets, databases) | Excels at unstructured data (text, images, audio) |

## Related Terms
- [Machine Learning](machine-learning.md) — the broader category deep learning belongs to
- [Parameters](parameters.md) — the settings deep learning models learn during training
- [LLM (Large Language Model)](tier2/llm.md) — a deep learning model specifically for language
