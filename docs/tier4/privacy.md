# Privacy

**Privacy in AI** concerns how personal data is collected, used, stored, and protected when building and deploying AI systems. It covers both the privacy of individuals whose data trains models and the privacy of people who interact with AI applications.

## The Simple Version

Every time you type into a chatbot, upload a photo for analysis, or use an AI-powered app, your data is being processed somewhere. Privacy questions include:
- Who can see what you typed?
- Is your conversation stored forever?
- Could your data be used to train models that others use?
- Can someone reverse-engineer your information from a trained model?

AI makes privacy particularly tricky because these systems often need massive amounts of personal data to work well — but collecting that data creates significant risks.

## Where Privacy Risks Come From

### Training Data Collection
Most AI models are trained on data scraped from the internet, which includes:
- Personal blog posts and forum comments with identifiable information
- Medical records, financial data, or other sensitive documents accidentally included in datasets
- Photos and videos of people who didn't consent to being used for training
- Private communications that were leaked or shared publicly

### Data Used at Inference Time
When you interact with an AI service:
- Your prompts may be logged and stored by the provider
- Conversations might be reviewed by human trainers (for RLHF)
- Usage patterns could be sold to advertisers or data brokers
- Metadata (when, where, how often you use it) creates a behavioral profile

### Model Memorization
Research has shown that some AI models can memorize and potentially reproduce specific examples from their training data — including:
- Exact quotes from copyrighted books
- Personal information from leaked databases
- Phone numbers, addresses, or other PII (personally identifiable information)

## Privacy Concerns by Context

| Context | Risk | Example |
|---------|------|---------|
| **Chatbots** | Conversations stored and potentially reviewed | Your therapy notes used to train a mental health model |
| **Healthcare AI** | Medical data exposure | Patient records in training data leading to identifiable outputs |
| **Workplace monitoring** | Employee behavior tracked by AI | Productivity tools logging every keystroke and break |
| **Surveillance** | Facial recognition, location tracking | AI-powered policing systems with questionable accuracy across demographics |
| **Social media** | Content analysis and recommendation | Algorithms learning your preferences to maximize engagement (and addiction) |

## Privacy Protections

### Technical Measures
- **Differential privacy** — adding statistical noise to data so individual records can't be identified while preserving overall patterns
- **Federated learning** — training models on devices locally without sending raw data to a central server
- **Encryption** — protecting data in transit and at rest
- **Data minimization** — collecting only the data strictly necessary for the task

### Legal/Policy Measures
- **GDPR** (EU) — gives individuals rights over their data, including the "right to be forgotten"
- **CCPA** (California) — similar consumer privacy protections in the US
- **AI-specific regulations** — emerging laws like the EU AI Act that impose requirements on high-risk AI systems

### Best Practices for Users
- Assume anything you type into a public AI service could be stored and reviewed
- Avoid sharing sensitive personal information (health, financial, legal) with AI tools
- Check privacy policies: does the provider use your data for training? Can you opt out?
- Use local/self-hosted models when privacy is critical

## What Privacy Is NOT

- **Not just about "secrets"** — privacy isn't only about hiding information; it's about control over how your data is used and who has access to it
- **Not solved by anonymization** — removing names from datasets doesn't always prevent identification (people can be re-identified through combinations of other attributes)
- **Not a binary issue** — privacy isn't just "private" or "public." There are many degrees of data protection and many stakeholders with different interests

## The Privacy-AI Tension

There's an inherent tension between AI capabilities and privacy:
- Better AI generally needs more data → more privacy risk
- Stronger privacy protections (data minimization, deletion rights) can reduce model quality
- Open models that anyone can inspect are harder to control for privacy violations
- Closed models with strict privacy guarantees limit independent auditing

Finding the right balance is one of the central challenges in responsible AI development.

## Why It Matters

Privacy isn't just a legal compliance issue — it's fundamental to trust. If people don't believe their data is safe, they won't use AI tools, which limits their benefits. As AI becomes more embedded in healthcare, finance, education, and daily life, privacy protections need to evolve alongside the technology itself. Understanding these issues helps you make informed choices about which AI tools to use and how to protect your information.

## Related Terms
- [Bias](bias.md) — biased models often result from problematic data collection practices
- [Open Source vs. Proprietary](open-source-vs-proprietary.md) — open models raise different privacy questions than closed ones
- [Copyright](copyright.md) — training data and intellectual property overlap with privacy concerns
