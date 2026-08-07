# Generative AI

## a. Background & Why
Generative AI refers to models that create new content — text, images, audio, video, or code — rather than only classifying or predicting a label for existing content. Earlier "discriminative" AI answered questions like "is this email spam or not?" Generative AI answers "write me an email" or "draw me an image." This became mainstream once models like GPT (text), DALL·E/Midjourney (images), and diffusion models matured enough to produce genuinely usable, high-quality output rather than crude approximations.

## b. Life Before It (Traditional Way) vs Now
**Before:** Creating content — copy, designs, illustrations, code, video — required a human specialist (writer, designer, developer) starting largely from a blank page each time, or reusing rigid templates. Iteration was slow: a new draft meant a new work cycle.

**Now:** A first draft — of a blog post, a UI mockup, a marketing image, a code function — can be generated in seconds, with humans shifting toward directing, curating, and refining rather than producing everything from scratch.

## c. What Changes/Differs Without It
Without generative AI, content production timelines stay tied to human throughput: one designer produces one set of concepts per day, one writer drafts one article at a time. Personalized content at scale (e.g., unique product descriptions for thousands of SKUs) becomes cost-prohibitive, so businesses default to generic, one-size-fits-all content.

## d. Benefits
- Dramatically speeds up first-draft creation across text, image, audio, video, and code
- Enables content personalization at a scale manual production can't match
- Lowers the skill/cost barrier to producing decent creative or technical drafts
- Useful for rapid prototyping and exploring many variations quickly

## e. Limitations
- Quality is inconsistent — output often needs human editing/review before use
- Raises IP and copyright questions (training data provenance, ownership of output)
- Can produce biased, generic, or subtly wrong content that looks polished (dangerous because it's convincing)
- Compute cost for image/video generation is notably higher than text
- Risk of misuse (deepfakes, misinformation, plagiarism)

## f. Real-Life & Business Examples
- **E-commerce:** Auto-generated product descriptions and images for large catalogs.
- **Software:** AI-generated boilerplate code, tests, and documentation.
- **Marketing:** Rapid generation of ad variants for A/B testing.
- **Media:** AI-assisted video editing, dubbing, and voiceover generation for localization.

## g. What This Means for an IT Product Owner
- Build human-in-the-loop review into any workflow where output goes external-facing or has legal/brand risk.
- Clarify IP ownership and usage rights for AI-generated assets before shipping features around them — this is a real legal question, not just a technical one.
- Set expectations that generative features speed up "first draft," not necessarily "final, ready-to-publish" — factor review time into your delivery estimates.
- Watch cost per generation closely, especially for image/video features, since it directly affects unit economics.
- Consider brand and trust risk: generic or off-brand AI content can quietly erode user trust if unchecked.