# Skill: /content-ideas — Endless Idea Generator

## What this does

Takes a seed topic and generates a full set of content angles using the 4A framework.
Output is a menu of distinct ideas, not variations of the same idea.

---

## When to use

Run `/content-ideas` when:
- You have a topic but don't know what angle to take
- You want to turn one idea into 10 without repeating yourself
- You're planning a content calendar and need variety
- You're stuck staring at a blank page

---

## The four inputs to collect

Before generating ideas, establish:

### 1. Topic (with specificity drill-down)
Start with what the user gives you. If it's too broad, push for specificity.

Levels of specificity:
- V1: "I want to write about SEO" → too broad
- V2: "I want to write about SEO for Webflow sites"
- V3: "I want to write about why Webflow sites struggle to rank on Google"
- V4: "I want to write about the 3 technical reasons Webflow sites don't get indexed — and how to fix them"

If the user gives you a V1 or V2 topic, ask one clarifying question to push them to V3 or V4 before generating ideas.

### 2. Credibility type
Ask or infer which applies:
- **Expert**: "I've done this / built this / lived this"
- **Curator**: "I've studied others who've done this"
- **Personal experience**: "I've been through this myself"

### 3. Audience: General or Niche?
- General = broader reach, lower engagement
- Niche = smaller reach, higher engagement and loyalty

If unclear, generate one of each and let the user choose.

### 4. Proven approach (structure)
After generating angles, suggest a structure for each:
- How To (steps)
- Lessons Learned
- Mistakes to Avoid
- Frameworks
- Lists
- Personal Story

---

## The 4A framework — generate one idea per quadrant

### Actionable (here's how)
Give the reader something they can do.
Best for: tutorials, step-by-step guides, checklists.
Angle: "Here's what to do and how to do it."

### Analytical (here are the numbers)
Give the reader data, patterns, or research.
Best for: market insights, trend analysis, case studies.
Angle: "Here's what the data shows and what it means."

### Aspirational (yes, you can)
Give the reader motivation through a real story.
Best for: personal stories, transformations, before/after.
Angle: "Here's how I or someone else did it — and you can too."

### Anthropological (here's why)
Give the reader a deeper explanation of behavior or belief.
Best for: opinion pieces, root cause analysis, cultural commentary.
Angle: "Here's the real reason this happens."

---

## Output format

```
CONTENT IDEAS: [Topic]
Credibility: [Expert / Curator / Personal experience]
Audience: [General / Niche: specify]

─────────────────────────────────────

ACTIONABLE
Angle: [one sentence description]
Draft headline: [working title]
Structure: [How To / Steps / Checklist]
Platform fit: [Article / LinkedIn / Both]

─────────────────────────────────────

ANALYTICAL
Angle: [one sentence description]
Draft headline: [working title]
Structure: [Data breakdown / Case study / Comparison]
Platform fit: [Article / LinkedIn / Both]

─────────────────────────────────────

ASPIRATIONAL
Angle: [one sentence description]
Draft headline: [working title]
Structure: [Personal story / Before-After / Transformation]
Platform fit: [Article / LinkedIn / Both]

─────────────────────────────────────

ANTHROPOLOGICAL
Angle: [one sentence description]
Draft headline: [working title]
Structure: [Opinion / Root cause / Cultural analysis]
Platform fit: [Article / LinkedIn / Both]

─────────────────────────────────────

RECOMMENDED NEXT STEP
[Which angle to pursue first and why — one sentence]
```

After output, ask: "Want to develop any of these into a full outline, or run `/headline` on one of these titles?"

Apply writing rules from `writing-rules.md`.
