# Tokens & Context Windows

## a. Background & Why
LLMs don't read text as whole words or letters — they break input into "tokens," small chunks of text (roughly ¾ of a word on average in English; a word like "unbelievable" might be split into "un," "believ," "able"). Everything the model reads and generates is counted in tokens, and this matters directly for cost, speed, and capability. The "context window" is the maximum number of tokens (input + output combined) a model can consider at once — its working memory for a single conversation or task. This exists because processing text has real computational cost that scales with length, so there has to be a limit.

## b. Life Before It (Traditional Way) vs Now
**Before:** Traditional software had no meaningful limit on how much data it could "consider" at once beyond hardware/storage limits — a database query could scan millions of rows without a conceptual ceiling on what could be "read" in one operation.

**Now:** An LLM can only directly reason over what fits inside its context window. Feed it a 500-page document and ask a question, and depending on the model's window size, it may simply not "see" the relevant part at all — this is a fundamentally new constraint product teams must design around.

## c. What Changes/Differs Without It
If context windows didn't exist as a constraint (unlimited context), you could hand a model your entire knowledge base, codebase, or document history and ask anything without extra engineering. Because the constraint is real, teams must design retrieval systems (fetching just the relevant chunks), summarization pipelines, or chunking strategies to work within limits — adding real architectural complexity to any AI feature working with large documents or long histories.

## d. Benefits (of Understanding Tokens/Context Windows)
- Understanding token limits lets teams design efficient, cost-aware features (shorter, well-structured prompts cost less and run faster)
- Awareness drives smarter architecture choices (retrieval-augmented generation instead of dumping everything into the prompt)
- Helps set realistic expectations for what a feature can and can't "remember" or reference in one go
- Enables accurate cost forecasting, since most LLM providers bill per token

## e. Limitations
- Larger context windows cost more and can be slower to process
- Even within the window, models can pay uneven attention to different parts of very long input ("lost in the middle" effect) — bigger isn't always fully reliable
- Conversations exceeding the window require summarization or truncation, risking loss of earlier context
- Token counts don't map cleanly to word counts, making length estimation tricky for non-technical stakeholders

## f. Real-Life & Business Examples
- **Legal tech:** Reviewing a 200-page contract may require chunking the document and retrieving only relevant clauses rather than pasting the whole thing into one prompt.
- **Customer support:** Long support chat histories get summarized periodically so the AI assistant doesn't lose earlier context or exceed the window.
- **Coding assistants:** Tools index a whole codebase but only pull in the relevant files/functions per query, since the full codebase won't fit in context.
- **Billing:** SaaS companies pricing AI features per-use must account for token cost per interaction, which varies with document/conversation length.

## g. What This Means for an IT Product Owner
- Factor token costs directly into your pricing/unit economics model — usage isn't flat-fee like traditional compute, it scales with input/output length.
- For any feature touching large documents, plan for retrieval or chunking architecture up front, not as a later fix — this affects timelines and technical design significantly.
- Set user expectations around memory/context limits, especially for long conversations or large files ("the assistant may not recall very early messages in a long chat").
- Include token/context limits in your technical requirements documents so engineering can design accordingly from day one.
- When comparing AI vendors/models, context window size is a real feature comparison point — not just a technical detail — since it affects what use cases are even possible.