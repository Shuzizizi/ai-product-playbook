# Prompt Engineering

## a. Background & Why
Prompt engineering is the practice of crafting the input (the "prompt") given to an LLM to reliably get the output you want. Because LLMs generate responses based on patterns learned from text, *how* you ask matters almost as much as *what* you ask — the same underlying question, phrased differently, structured differently, or given different examples, can produce very different quality output. This discipline emerged because early users found that vague prompts got vague, inconsistent, or unhelpful results, while well-structured prompts (clear instructions, examples, defined format) got dramatically better ones.

## b. Life Before It (Traditional Way) vs Now
**Before:** Getting software to do something meant writing code — precise, unambiguous instructions in a programming language. There was no "how you phrase it" variable; the computer either had the function or it didn't.

**Now:** Natural language itself is the interface. A product manager, support agent, or analyst with no coding background can shape an AI system's behavior just by writing clearer instructions — but this also means quality now depends on prompt-writing skill, which is a genuinely new and unevenly distributed skill across teams.

## c. What Changes/Differs Without It
Without deliberate prompt engineering, teams get inconsistent, lower-quality AI output — vague instructions produce vague answers, missing context leads to hallucination or irrelevant responses, and there's no repeatable, testable way to get the same quality of result twice. Features built on ad-hoc prompts tend to be fragile and hard to debug when they misbehave.

## d. Benefits
- Meaningfully improves output quality and consistency without touching the underlying model
- Cheap and fast to iterate on compared to retraining or fine-tuning a model
- Enables non-engineers to shape AI behavior directly
- Can encode business rules, tone, and constraints directly into how a feature behaves
- Supports techniques like step-by-step reasoning, examples (few-shot), and structured output formats that measurably reduce errors

## e. Limitations
- No prompt fully guarantees correctness — it reduces but doesn't eliminate hallucination or inconsistency
- Prompts that work well on one model version may behave differently after a model update
- Over-engineered prompts can become long, brittle, and expensive (more tokens = more cost/latency)
- Hard to "test" prompts with the same rigor as traditional code without a proper evaluation framework
- Prompt injection (malicious input trying to override instructions) is a real security concern in production

## f. Real-Life & Business Examples
- **Internal tools:** A company writes a detailed system prompt so a support-ticket summarizer always outputs the same structured format (issue, sentiment, priority) instead of freeform text.
- **Content moderation:** Prompt design that explicitly defines edge cases reduces false positives/negatives in AI-assisted moderation.
- **Coding assistants:** Providing the assistant a style guide and examples in the prompt produces code that matches a team's conventions.
- **Sales enablement:** Prompting a model with company-specific product details and tone guidelines produces on-brand outreach drafts instead of generic ones.

## g. What This Means for an IT Product Owner
- Treat prompts as a versioned, testable product artifact — not a throwaway string buried in code. Track changes and their impact on output quality.
- Budget time for prompt iteration and evaluation as part of the delivery timeline, not as a "quick tweak" at the end.
- Understand that prompt changes can shift behavior across the whole feature — regression testing matters here too.
- Be aware of prompt injection risk if any part of the prompt includes untrusted user input or external content.
- Recognize prompt engineering as a cross-functional skill — good prompts often come from domain experts (support, legal, marketing), not just engineers, so involve them early.