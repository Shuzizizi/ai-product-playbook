# LLM (Large Language Model)

## a. Background & Why
A Large Language Model is an AI system trained on massive amounts of text to predict and generate human-like language. The "large" refers to both the size of the training data (often a significant chunk of the public internet plus curated sources) and the number of parameters (billions to trillions). The breakthrough architecture — the Transformer (2017) — allowed models to weigh the relevance of every word against every other word in a passage, which unlocked much better language understanding and generation than earlier approaches (like rule-based NLP or simpler statistical models).

## b. Life Before It (Traditional Way) vs Now
**Before:** Natural Language Processing relied on hand-crafted rules, keyword matching, or narrow statistical models trained for one specific task (e.g., a spam classifier could only classify spam — nothing else). Chatbots followed rigid decision trees; asking anything outside the script broke them.

**Now:** A single LLM can draft emails, summarize documents, answer questions, translate, write code, and hold open-ended conversations — all from the same underlying model, often with no task-specific retraining, just a well-written prompt.

## c. What Changes/Differs Without It
Without LLMs, teams need separate, purpose-built models or systems for each language task (translation engine, summarizer, classifier, chatbot script), each requiring its own dataset and maintenance. Natural, flexible conversation with software isn't possible — users must adapt to rigid menus, forms, or keyword commands instead of the system adapting to them.

## d. Benefits
- One general-purpose model handles many language tasks (drafting, summarizing, coding, Q&A, translation)
- Understands context and nuance far better than keyword or rule-based systems
- Fast to prototype with — often just a prompt, no model training required
- Can be fine-tuned or grounded (e.g., via retrieval) on company-specific knowledge

## e. Limitations
- Can "hallucinate" — generate confident but false information (see hallucination.md)
- Costly to run at scale (compute-intensive, especially larger models)
- Knowledge is frozen at training time unless connected to external/live data
- Sensitive to how a prompt is phrased — inconsistent prompting gives inconsistent output
- Can inherit biases present in training data

## f. Real-Life & Business Examples
- **Customer service:** LLM-powered assistants draft or fully answer support tickets, reducing handling time.
- **Legal/Compliance:** LLMs summarize lengthy contracts and flag risky clauses for review.
- **Software engineering:** Coding assistants (e.g., Claude Code, GitHub Copilot) generate and explain code, speeding up development.
- **Marketing:** Teams use LLMs to draft first versions of ad copy, product descriptions, and emails.

## g. What This Means for an IT Product Owner
- LLM output is probabilistic — plan for review/approval steps in workflows where errors are costly (legal, medical, financial).
- Cost scales with usage (tokens processed) — factor this into the business case, not just development cost.
- Prompt design and grounding (giving the model the right context) becomes a real product/design discipline, not just an engineering detail.
- Data privacy matters: know whether prompts/data sent to an LLM provider are used for training and where they're stored.
- Define clear boundaries for what the LLM is allowed to decide autonomously vs. what requires human sign-off.