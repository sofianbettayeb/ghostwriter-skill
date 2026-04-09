# Skill: /post — LinkedIn Post Builder

## What this does

Builds or improves a LinkedIn post using platform-specific rules.
Not a generic social post formatter. LinkedIn has its own algorithm, format, and audience behavior.

---

## When to use

Run `/post` when:
- You want to turn an idea, article, or draft into a LinkedIn post
- You have a post draft that isn't performing or feels flat
- You want to adapt an existing article into LinkedIn format
- You're creating original LinkedIn content from scratch

---

## LinkedIn-specific rules (non-negotiable)

### The hook — 5 lines max
LinkedIn cuts off posts after 5 lines with a "See More" button.
The algorithm treats a click on "See More" as an engagement signal.
Your hook must earn that click.

Hook rules:
- Tease what's inside without giving it away
- State the transformation or value the reader will get
- Create a curiosity gap — beginning + end, but not the middle
- Never waste line 1 on context-setting or throat-clearing

### Post structure
Three parts, in this order:
1. **Hook** (5 lines max): grab attention, earn the "See More" click
2. **Main points**: deliver on the hook's promise
3. **Engagement question**: ask something that invites a response

### CTA placement
Never put links in the post body. LinkedIn suppresses reach on posts with outbound links.
Always put the CTA (link, resource, offer) in the first comment.
Note this in the output so the user knows to do it.

### Formatting
- Short sentences. One idea per line.
- Use carriage returns liberally — white space is skimmability.
- Pattern: one sentence + 3 bullets works well
- No walls of text. If it looks dense, it won't be read.

---

## The 6 content types — pick one per post

### 1. Actionable
Give the reader something they can do today.
Format: steps, checklist, how-to
Best for: tutorials, process breakdowns, quick wins

### 2. Aspirational
A personal story with a transformation.
Format: before → struggle → turning point → after
Best for: building trust, humanizing expertise, standing out in a sea of tips posts

### 3. Framework
A named, structured way to think about a problem.
Format: name the framework → explain each part → show how to use it
Best for: thought leadership, establishing a point of view

### 4. Curated list
A collection of things your audience finds valuable.
Format: people to follow / tools to use / resources to read
Best for: low-effort high-reach, community building

### 5. Contrarian take
Disagree with conventional wisdom on your topic.
Format: "Everyone says X. Here's why that's wrong." → your actual view → evidence
Best for: standing out, sparking conversation, testing an opinion

### 6. Professional entertainment
Industry-relevant, but not boring.
Format: pop-culture reference or unexpected analogy → connect to your topic → takeaway
Best for: breaking the LinkedIn monotony, building personality

---

## Engagement question formats

End every post with one question. Types that work:
- "What would you add?"
- "Which of these have you tried?"
- "Am I wrong about this?"
- "What's your take?"
- "Drop yours in the comments."

Avoid: "Let me know your thoughts!" (too vague, no traction)

---

## Output format

```
LINKEDIN POST: [topic / content type]

─────────────────────────────────────
HOOK (5 lines):
[Lines 1–5 of the post]

MAIN POINTS:
[Body of the post]

ENGAGEMENT QUESTION:
[Closing question]

─────────────────────────────────────
CTA (post in comments):
[Link or resource to drop in first comment]

─────────────────────────────────────
NOTES:
Content type: [Actionable / Aspirational / Framework / List / Contrarian / Entertainment]
Hook strength: [strong / needs work — reason]
Formatting: [ready / needs spacing / needs bullets]
```

If editing an existing post, show before/after with notes on what changed.
Apply writing rules from `writing-rules.md`.
