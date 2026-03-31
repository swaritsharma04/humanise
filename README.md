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

- **Banned AI vocabulary** — words like *delve*, *tapestry*, *vibrant*, *crucial*, *pivotal*, *landscape* (figurative), *testament*, *showcase*, *foster*, and dozens more.
- **Banned sentence openers** — *Discover*, *Explore*, *Remember*, *Delve*, *Transform*, etc.
- **Em dashes** — replaced with commas, periods, colons, or parentheticals.
- **Legacy/significance filler** — hollow sentences about "enduring legacies" and "pivotal moments" get deleted.
- **Rule-of-three patterns** — the classic AI habit of grouping everything in threes.
- **Negative parallelisms** — "Not just X, but also Y" constructions.
- **Promotional puffery** — travel-brochure and press-release language flattened to plain facts.
- **Weasel attributions** — "Experts argue..." replaced with named sources or deleted.
- **Didactic throat-clearing** — "It's important to note..." removed.
- **Monotonous sentence rhythm** — varied to sound like actual human writing.

## Installation

1. Download the `.skill` file.
2. In Claude.ai, go to **Settings → Skills**.
3. Upload the `.skill` file.

### Or install from source

1. Clone this repo.
2. Zip the `humanise/` folder (the folder itself must be the root entry in the zip):
   ```bash
   zip -r humanise.skill humanise/
   ```
3. Upload `humanise.skill` to Claude.

## License

MIT — see [LICENSE](LICENSE).
