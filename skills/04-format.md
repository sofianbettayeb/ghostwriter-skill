# Skill: /format — Formatting & Rhythm

## What this does

Two things in one skill:
1. Restructures a draft for skimmability (skeleton, subheads, bullets)
2. Analyzes and fixes writing rhythm (sentence patterns, rate of revelation)

Run together by default. Run separately if the user specifies.

---

## When to use

Run `/format` when:
- A draft reads like a wall of text
- The writing feels flat or monotone
- You want to check rhythm before publishing
- You're turning a rough draft into something readable

---

## Part 1: Skimmability

### The skeleton check
Every piece needs a clear skeleton before you worry about prose.

Check for:
- **Headline**: Does it answer WHO / WHAT / WHY? (If not, flag and suggest running `/headline`)
- **Introduction**: Does it repeat the headline's promise with slightly more detail? Does it establish credibility?
- **Main points**: Is there a clear organizing structure? (Steps / Lessons / Mistakes / Tips)
- **Conclusion**: Is there a final takeaway, or does the piece just stop?

### Wheels & Spokes
- **Wheels** (H2): Big section headings. Mark the start of a new idea.
- **Spokes** (H3): Subheadings within a section. Separate sub-ideas.

For short pieces (300–800 words): one level of headings is enough.
For long pieces (800+ words): use both Wheels and Spokes.

### Bullets and lists
Anytime a paragraph lists 3+ things in prose, convert to bullets.
Before: "You should check your meta titles, your canonical tags, and your sitemap submission status."
After:
- Meta titles
- Canonical tags
- Sitemap submission status

### Visual rhythm rule
Readers skim before they read.
If the page looks dense, they leave.
Short paragraphs + subheads + occasional bullets = readable at a glance.

---

## Part 2: Writing Rhythm

### The patterns to check for

**Good rhythms** (alternating short and long):
- 1/3/1: Single opener → 3-sentence body → Single closer
- 1/5/1: Single opener → 5-sentence body → Single closer
- 1/2/5/2/1: Build up, peak, build back down (crescendo/decrescendo)
- Stacked 1/3/1 + 1/3/1: Two sequences in a row

**Bad rhythms** (monotone):
- 1/1/1/1/1: Every sentence its own paragraph. Reads frantic.
- 5/5/5: Every paragraph the same length. Reads like a textbook.
- 2/2/2: Monotone. No movement.

### Rate of Revelation check
Every sentence should move the idea forward.
Ask for each sentence: "Am I saying something new, or repeating what I just said?"

Slow (bad):
> "When it comes to building a writing habit, the most important thing is just sitting down and writing. It can be hard, but that's part of it. All writers go through this."

Fast (good):
> "Three things usually block a daily writing habit: over-editing, self-doubt, and a dead laptop battery at the coffee shop."

Flag any paragraph where consecutive sentences repeat the same point in different words.

---

## Output format

Return the formatted draft with inline notes in brackets.

```
FORMATTING AUDIT

SKELETON: [complete / missing introduction / missing conclusion / no structure]
SKIMMABILITY: [ready / needs subheads / needs bullet conversion / too dense]
RHYTHM PATTERN FOUND: [e.g., 2/2/2/2 — monotone]
RATE OF REVELATION: [fast / slow — [location of main issue]]

---

REVISED DRAFT:

[Full revised draft with formatting applied]

[RHYTHM NOTE: paragraph X changed from 5/5 to 1/3/1]
[BULLET NOTE: list converted from prose]
[SUBHEAD ADDED: "X" — separates idea Y from idea Z]
```

If the piece is already well-formatted, say so in one sentence and skip the revision.
Apply writing rules from `writing-rules.md`.
