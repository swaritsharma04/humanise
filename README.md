# Humanise (Claude Skill)

A custom skill for [Claude](https://claude.ai) that rewrites AI-generated text to sound like a human wrote it.

## What it does

Humanise takes any AI-generated prose and aggressively rewrites it: restructuring sentences, varying rhythm, purging telltale AI vocabulary, and cutting filler. Every substantive point is preserved, but the robotic tone is stripped out.

Works on blog posts, articles, academic writing, marketing copy, reports, and any other prose.

## Trigger phrases

The skill activates when you say things like:

- "humanise this" / "humanize this"
- "make it sound human"
- "remove AI tone"
- "rewrite naturally"
- "sound less robotic"
- "de-AI this"

## What it catches

- **Banned AI vocabulary** words like *delve*, *tapestry*, *vibrant*, *crucial*, *pivotal*, *landscape* (figurative), *testament*, *showcase*, *foster*, and dozens more.
- **Banned sentence openers** like *Discover*, *Explore*, *Remember*, *Delve*, *Transform*, etc.
- **Em dashes** to be replaced with commas, periods, colons, or parentheticals.
- **Legacy/significance filler** like hollow sentences about "enduring legacies" and "pivotal moments" get deleted.
- **Rule-of-three patterns** like the classic AI habit of grouping everything in threes.
- **Negative parallelisms**. "Not just X, but also Y" constructions.
- **Promotional puffery** like travel-brochure and press-release language flattened to plain facts.
- **Weasel attributions** like "Experts argue..." replaced with named sources or deleted.
- **Didactic throat-clearing** like "It's important to note..." removed.
- **Monotonous sentence rhythm** now varied to sound like actual human writing.

## Installation

1. Download the `.skill` file.
2. In Claude.ai, go to **Settings → Skills**.
3. Upload the `.skill` file.

## License

MIT: see [LICENSE](LICENSE).
