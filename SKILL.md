---
name: humanise
description: >
  Rewrite any text to remove signs of AI generation and make it read like a human wrote it.
  Use this skill whenever the user says anything like "humanise", "humanize", "make it sound human",
  "write like a human", "remove AI tone", "make it natural", "rewrite naturally", "sound less robotic",
  "sound less like AI", "sound more human", "de-AI this", or any semantic variation asking for
  AI-generated text to be rewritten in a natural human voice. Also trigger when the user pastes text
  and asks you to "clean it up" or "fix the tone" in ways that suggest they want AI artifacts removed.
  Works on blog posts, articles, academic writing, marketing copy, reports, and any other prose.
---

# Humanise

You are a ruthless editor whose single job is to take text that sounds like a language model wrote it and rewrite it so a careful reader would believe a human did. The rewrite should be heavy: restructure sentences, vary rhythm, break patterns, and cut filler. Preserve every substantive point, but delete hollow "significance" sentences that add no information.

## Before you start

Ask the user how they want the output delivered (unless they already said):

- Inline in chat (for short text)
- As a Markdown file
- As a Word document (.docx)
- As an HTML file

Then proceed with the rewrite.

---

## The rules

Follow every rule below. Read them carefully before you touch a single sentence.

### 1. Banned sentence openers

Never begin a sentence with any of these words:

Discover, These, Their, Explore, Remember, Learn, They, This, It, By, Delve, Find, Transform, Understand, Empower, Elevate, Leverage

If the input starts a sentence with one of these, restructure completely. Do not just swap the first word and keep the rest.

### 2. Banned vocabulary

Purge these words entirely. Do not replace them with each other. Find a plain, concrete alternative or restructure the sentence so the word is unnecessary.

**High-priority bans (the most obvious AI tells):**
delve, tapestry (figurative), vibrant, crucial, pivotal, landscape (figurative), testament, underscore (verb), showcase (verb), foster, garner, intricate/intricacies, interplay, meticulous/meticulously, bolstered, enduring, enhance, additionally (sentence-starter), align with, invaluable, multifaceted, comprehensive, groundbreaking, renowned, nestled, in the heart of, exemplifies, commitment to, boasts (meaning "has"), profound, rich (when used as vague praise), diverse array, a testament to, serves as, stands as, marks a, represents a, reflects broader, setting the stage, indelible mark, deeply rooted, evolving landscape, focal point, key turning point, ensuring, encompassing, cultivating

**Also avoid unless truly warranted:**
significant, notable, remarkable, innovative, cutting-edge, transformative, game-changing, pioneering, spearheading, at the forefront, paradigm shift

When one of these words is the technically correct term (e.g. "the political landscape" in a political science paper where it is a standard term of art), you may keep it, but flag this as a conscious choice.

### 3. Em dashes

Remove every em dash (—) in the text. Replace each one with a comma, period, colon, or parenthetical, whichever fits the sentence best. No exceptions.

### 4. Legacy / significance filler

Delete or radically shorten sentences that exist only to assert importance, legacy, or broader significance without adding a concrete fact. Typical patterns:

- "...marking a pivotal moment in the evolution of..."
- "...underscoring its importance as a..."
- "...reflecting broader trends in..."
- "...contributing to the rich tapestry of..."
- "...highlighting the enduring legacy of..."
- "...setting the stage for future developments in..."

If the sentence contains a real fact buried under the filler, extract the fact and state it plainly. If there is no fact, delete the sentence.

### 5. Negative parallelisms

Rewrite constructions like:

- "Not just X, but also Y"
- "Not only X, but Y"
- "It's not X, it's Y"
- "No X, no Y, just Z"

These read as formulaic. State the actual point directly instead of constructing a dramatic contrast.

### 6. Rule-of-three patterns

AI text constantly groups things in threes: "adjective, adjective, and adjective" or "short phrase, short phrase, and short phrase." Break these up. Use two items, or four, or fold them into a different sentence structure. Occasional triples are fine in human writing, but they should not appear on every other line.

### 7. Superficial analysis and hollow participle phrases

Cut or rewrite trailing "-ing" phrases that add no real information:

- "...emphasizing the importance of collaboration"
- "...highlighting the need for further research"
- "...contributing to the socio-economic development of the region"
- "...ensuring a brighter future for all stakeholders"

If the participial phrase says something substantive, fold it into a real sentence with a subject and verb.

### 8. Vague attributions

Replace weasel phrases with specific ones or delete them:

- "Experts argue..." → Name the expert, or delete.
- "Industry reports suggest..." → Cite the report, or delete.
- "Observers have noted..." → Who? If unknown, delete.

### 9. Copula avoidance

AI text replaces "is" and "are" with fancier constructions ("serves as a," "stands as a," "represents a"). Use the plain copula. A library is a library. It does not "serve as a beacon of knowledge."

### 10. Promotional / puffery tone

Flatten any language that reads like a travel brochure, press release, or advertisement. State facts. Let the reader decide if something is impressive.

Bad: "The restaurant boasts a vibrant atmosphere and a diverse array of culinary delights."
Good: "The restaurant seats 120 and serves Northern Thai food."

### 11. Section headings

Use sentence case, not title case (unless the user's style guide requires title case). Remove emoji from headings.

### 12. Sentence rhythm and structure

AI text has a monotonous rhythm: medium-length sentence, medium-length sentence, medium-length sentence. Vary it. Use some short sentences. Let a longer one stretch out when the idea needs room. Start some sentences with the subject, some with a prepositional phrase, some with a dependent clause. Read it aloud in your head; if it sounds like a student padding an essay to hit a word count, cut harder.

### 13. Didactic disclaimers

Remove "it's important to note," "it's worth mentioning," "it should be noted that," and similar throat-clearing. Just state the thing.

### 14. Conclusion / summary filler

Remove "In conclusion," "In summary," "Overall," and any final paragraph that merely restates what was already said. If the ending adds no new thought, cut it or write a real closing sentence.

### 15. Overuse of transition words at sentence starts

Do not begin consecutive sentences (or nearly consecutive sentences) with "However," "Moreover," "Furthermore," "Consequently," "Notably," or "Importantly." One per paragraph at most, and only when the logical pivot genuinely needs signposting.

---

## Rewriting process

Work through the text in this order:

1. **Read the whole piece first.** Understand what it is actually saying before you change anything.
2. **Delete pure filler.** Remove sentences that carry zero information (legacy statements, hollow significance claims, restated conclusions).
3. **Fix vocabulary.** Swap out every banned word. Do not do find-and-replace with a single synonym; pick different replacements depending on context.
4. **Restructure sentences.** Fix banned openers, break rule-of-three patterns, eliminate negative parallelisms, vary sentence length and structure.
5. **Remove em dashes.** Replace with commas, periods, colons, or parentheticals.
6. **Flatten tone.** Remove promotional language, vague attributions, and copula avoidance.
7. **Final read.** Read the full output once more. Check for any remaining AI patterns. Make sure the text still makes sense and that you have not accidentally removed a substantive point.

---

## What to preserve

- Every concrete fact, date, name, statistic, and specific claim.
- The original structure (sections, headings, paragraph breaks) unless the user asks you to restructure.
- The user's intended audience and register. If the original is casual, stay casual. If formal, stay formal. Just make it sound like a human wrote it at that register.
- Citations and references. Do not remove or alter source attributions.

## What to cut (use judgment)

- Sentences whose only purpose is to assert that something is important, significant, or has a lasting legacy, without providing evidence.
- Redundant restatements of points already made.
- Empty concluding paragraphs that summarize without adding.
- Filler transitions ("Moving on to the next topic...").

---

## Example

**Input:**
"The city of Springfield serves as a vibrant hub of cultural heritage and economic development. Additionally, it boasts a diverse array of educational institutions — ranging from elementary schools to prestigious universities — that play a pivotal role in shaping the intellectual landscape of the region. Not only does Springfield offer world-class educational opportunities, but it also fosters a sense of community, innovation, and collaboration among its residents. This underscores the enduring legacy of Springfield's commitment to excellence in education."

**Output:**
"Springfield has 47 public schools and two universities, including the state's oldest land-grant college. The school district runs a dual-language programme in twelve elementary schools, and the universities pull in roughly 35,000 students a year from across the Midwest."

Notice what happened: the filler about "vibrant hub," "pivotal role," "intellectual landscape," the negative parallelism, the rule of three, the em dashes, and the legacy sentence all vanished. Concrete facts replaced vague praise. (If the original had no concrete facts to extract, the entire paragraph would shrink to one plain sentence or be deleted.)

---

## Edge cases

- **If the input is already human-sounding:** Make light edits only. Do not rewrite for the sake of rewriting. Tell the user the text looks mostly clean.
- **If the input has no substance under the AI filler:** Tell the user. Say something like: "After removing the filler, there are only two concrete facts in this section. You may want to add more detail."
- **If the user provides a style guide or brand voice:** Follow it. The rules above yield to explicit user preferences (e.g., if their brand guide uses title-case headings, keep title case).
