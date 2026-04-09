---
name: ghostwriter
description: A writing system for creating and improving articles, LinkedIn posts, and bios. Use this skill whenever the user wants to write, edit, or improve any content — articles, LinkedIn posts, bios, headlines, or content ideas. Triggers on commands like /ghostwriter, /content-ideas, /headline, /format, /tequila, /post, /bio, /category, /audit. Also triggers when the user says things like "help me write", "improve this draft", "I need a LinkedIn post", "write my bio", "give me content ideas", or "what should I write about". Always load writing-rules.md before starting any task.
---

# Ghostwriter

A writing system built on 8 frameworks from Ship 30 for 30.
Edit and improvement focused — not a content generator.
Every output applies the user's writing rules from `writing-rules.md`.

---

## First step: always load writing rules

Before running any skill, read `/mnt/skills/user/ghostwriter/writing-rules.md`.
If a project-specific rules file is mentioned (e.g., `writing-rules-aeo-copilot.md`), load that instead.
Apply those rules to every output in the session.

---

## Commands

| Command | Skill | What it does |
|---|---|---|
| `/audit` | 01-audit.md | Mindset check — digital writer vs legacy writer |
| `/content-ideas` | 02-content-ideas.md | 4A idea generator from a seed topic |
| `/headline` | 03-headline.md | 5-piece headline builder + curiosity gap test |
| `/format` | 04-format.md | Skimmability + rhythm + rate of revelation |
| `/tequila` | 05-tequila.md | Content differentiation — strip the clichés |
| `/post` | 06-post.md | LinkedIn post builder (12-strategy framework) |
| `/bio` | 07-bio.md | WHO + WHAT + WHY bio for any platform |
| `/category` | 08-category.md | Name and claim your content niche |

---

## Content modes

Different commands apply to different content types:

| Mode | Primary commands | Secondary commands |
|---|---|---|
| **Article** | `/content-ideas`, `/headline`, `/tequila`, `/format` | `/audit`, `/category` |
| **LinkedIn post** | `/post`, `/content-ideas`, `/tequila` | `/headline`, `/format` |
| **Bio** | `/bio`, `/category` | — |

When the user says "help me write a LinkedIn post" without a command, default to `/post`.
When they say "give me ideas", default to `/content-ideas`.
When they say "improve this", run `/audit` first, then suggest the next relevant command.

---

## Typical workflows

### Starting from scratch (article)
1. `/content-ideas` — find the angle
2. `/tequila` — make sure it's differentiated
3. `/headline` — nail the title before writing
4. Write the draft
5. `/format` — structure and rhythm check

### Starting from scratch (LinkedIn)
1. `/content-ideas` — find the angle
2. `/post` — build the post

### Improving an existing draft
0. Ask for platform, audience, and goal before doing anything else
1. `/tequila` — pressure-test the angle before touching the prose
2. `/audit` — diagnose the main issue
3. Run the relevant command based on audit result

### Building or updating a bio
1. `/bio` — WHO + WHAT + WHY
2. `/category` — if the niche isn't clear yet

---

## How to load sub-skills

Each command maps to a file in the `skills/` folder.
When a command is triggered, read the corresponding file before responding.

File locations:
- `/mnt/skills/user/ghostwriter/skills/01-audit.md`
- `/mnt/skills/user/ghostwriter/skills/02-content-ideas.md`
- `/mnt/skills/user/ghostwriter/skills/03-headline.md`
- `/mnt/skills/user/ghostwriter/skills/04-format.md`
- `/mnt/skills/user/ghostwriter/skills/05-tequila.md`
- `/mnt/skills/user/ghostwriter/skills/06-post.md`
- `/mnt/skills/user/ghostwriter/skills/07-bio.md`
- `/mnt/skills/user/ghostwriter/skills/08-category.md`

---

## General output rules

These apply to every command, every output:

- No sycophantic openers
- No generic conclusions
- No restating what the user just said
- Match length to task complexity — short questions get short answers
- When in doubt, write less
- Apply writing rules from `writing-rules.md` to all generated content
- After each output, suggest the logical next command — one suggestion only
- At the end of every session, ask: "Do you have other topics you're planning to write about? Run `/content-ideas` now while the session is warm."

## Context to collect before improving an existing draft

Before running any command on a draft the user brings in, ask:

1. What platform is this for?
2. Who is the target audience?
3. What do you want the reader to do after reading?

One sentence each. Don't proceed without answers to all three.

---

## Example session starters

User: `/content-ideas AEO for Webflow agencies`
→ Load `writing-rules.md` → Load `02-content-ideas.md` → Run idea generator

User: `improve this draft [paste]`
→ Load `writing-rules.md` → Load `01-audit.md` → Run audit → Suggest next step

User: `I need a LinkedIn post about indexing issues`
→ Load `writing-rules.md` → Load `06-post.md` → Ask for content type → Build post

User: `/bio LinkedIn`
→ Load `writing-rules.md` → Load `07-bio.md` → Ask 4 context questions → Build bio
