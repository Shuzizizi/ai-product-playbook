# AI (Artificial Intelligence)

## a. Background & Why
Artificial Intelligence refers to computer systems built to perform tasks that normally require human intelligence — recognizing patterns, making decisions, understanding language, and learning from data instead of following only fixed, hand-written rules. The idea dates back to the 1950s, but it stayed largely academic for decades because compute power, data, and algorithms weren't mature enough. The "why now" is simple: cheap cloud compute, massive datasets, and better algorithms (especially deep learning since ~2012) finally made AI practical and affordable enough for everyday products, not just research labs.

## b. Life Before It (Traditional Way) vs Now
**Before:** Software worked purely on explicit logic — "if X, then Y." Every case had to be anticipated and coded by a developer. Handling ambiguity (e.g., understanding a customer's free-text complaint) required either armies of manual reviewers or brittle keyword-matching rules that broke easily.

**Now:** Systems can learn patterns from historical data and generalize to new, unseen situations. Instead of writing rules for every scenario, teams train or fine-tune a model on examples and let it infer the logic. This shifts effort from "coding every rule" to "curating good data and evaluating model behavior."

## c. What Changes/Differs Without It
Without AI, products fall back to static rules, manual triage, and human-only judgment calls. Tasks like fraud detection, personalized recommendations, spam filtering, or document summarization either don't scale, require large ops teams, or simply don't get built because the "if-then" cost is too high. Decision speed drops, personalization becomes generic (segment-based instead of individual-based), and edge cases pile up as manual backlog.

## d. Benefits
- Automates cognitively demanding tasks at scale (image recognition, language understanding, forecasting)
- Learns and improves as more data becomes available
- Enables personalization at an individual level, not just by broad segment
- Frees human effort for judgment-heavy, ambiguous, or relationship-driven work
- Can surface patterns humans would miss in large datasets

## e. Limitations
- Requires quality data — biased or incomplete data produces biased or wrong outputs
- Often a "black box": harder to explain exactly why a decision was made
- Can fail unpredictably on inputs unlike its training data (edge cases, adversarial inputs)
- Needs ongoing monitoring/retraining — performance can degrade ("drift") over time
- Ethical, legal, and regulatory risk (bias, privacy, accountability) is real and growing

## f. Real-Life & Business Examples
- **Banking:** AI-driven fraud detection flags unusual transaction patterns in real time, reducing losses versus static rule engines.
- **Retail (e.g., Amazon):** Recommendation engines drive a large share of purchases by predicting individual preference.
- **Healthcare:** AI-assisted imaging tools help radiologists flag potential tumors faster.
- **Customer Support:** AI triage routes and drafts responses to tickets, cutting first-response time.

## g. What This Means for an IT Product Owner
- Treat data quality and availability as a first-class product requirement, not an afterthought.
- Success metrics shift from "does the feature work" to "does the model perform well enough, and how do we know" — you need evaluation criteria, not just acceptance criteria.
- Plan for a feedback loop: monitoring, retraining, and drift detection are ongoing product work, not one-time delivery.
- Get comfortable owning trade-offs around explainability, fairness, and risk — these are product decisions, not just engineering ones.
- Set realistic expectations with stakeholders: AI features are probabilistic, not deterministic — "it works most of the time, in known ways" is the honest framing.