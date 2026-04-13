---
name: ghostwriter
description: A writing system for creating and improving articles, LinkedIn posts, and bios. Use this skill whenever the user wants to write, edit, or improve any content — articles, LinkedIn posts, bios, headlines, or content ideas. Triggers on commands like /ghostwriter, /ghostwriter:audit, /ghostwriter:content-ideas, /ghostwriter:headline, /ghostwriter:format, /ghostwriter:tequila, /ghostwriter:post, /ghostwriter:bio, /ghostwriter:category. Also triggers when the user says things like "help me write", "improve this draft", "I need a LinkedIn post", "write my bio", "give me content ideas", or "what should I write about". Always load writing-rules.md before starting any task.
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

When `/ghostwriter` is called with no subcommand, print this menu and wait:

```
Ghostwriter is loaded. What do you want to do?

/ghostwriter:audit          — is your writing digital or legacy?
/ghostwriter:tequila        — is your angle differentiated?
/ghostwriter:headline       — build a stronger title
/ghostwriter:format         — fix structure and rhythm
/ghostwriter:content-ideas  — generate angles from a seed topic
/ghostwriter:post           — build a LinkedIn post
/ghostwriter:bio            — WHO + WHAT + WHY bio
/ghostwriter:category       — name your content niche
```

| Command | Skill | What it does |
|---|---|---|
| `/ghostwriter:audit` | 01-audit.md | Mindset check — digital writer vs legacy writer |
| `/ghostwriter:content-ideas` | 02-content-ideas.md | 4A idea generator from a seed topic |
| `/ghostwriter:headline` | 03-headline.md | 5-piece headline builder + curiosity gap test |
| `/ghostwriter:format` | 04-format.md | Skimmability + rhythm + rate of revelation |
| `/ghostwriter:tequila` | 05-tequila.md | Content differentiation — strip the clichés |
| `/ghostwriter:post` | 06-post.md | LinkedIn post builder (12-strategy framework) |
| `/ghostwriter:bio` | 07-bio.md | WHO + WHAT + WHY bio for any platform |
| `/ghostwriter:category` | 08-category.md | Name and claim your content niche |

---

## Content modes

Different commands apply to different content types:

| Mode | Primary commands | Secondary commands |
|---|---|---|
| **Article** | `/ghostwriter:content-ideas`, `/ghostwriter:headline`, `/ghostwriter:tequila`, `/ghostwriter:format` | `/ghostwriter:audit`, `/ghostwriter:category` |
| **LinkedIn post** | `/ghostwriter:post`, `/ghostwriter:content-ideas`, `/ghostwriter:tequila` | `/ghostwriter:headline`, `/ghostwriter:format` |
| **Bio** | `/ghostwriter:bio`, `/ghostwriter:category` | — |

When the user says "help me write a LinkedIn post" without a command, default to `/ghostwriter:post`.
When they say "give me ideas", default to `/ghostwriter:content-ideas`.
When they say "improve this", run `/ghostwriter:tequila` first (not `/ghostwriter:audit`), then `/ghostwriter:audit`, then the relevant command.

---

## Typical workflows

### Starting from scratch (article)
1. `/ghostwriter:content-ideas` — find the angle
2. `/ghostwriter:tequila` — make sure it's differentiated
3. `/ghostwriter:headline` — nail the title before writing
4. Write the draft
5. `/ghostwriter:format` — structure and rhythm check

### Starting from scratch (LinkedIn)
1. `/ghostwriter:content-ideas` — find the angle
2. `/ghostwriter:post` — build the post

### Improving an existing draft
0. Ask for platform, audience, and goal before doing anything else
1. `/ghostwriter:tequila` — pressure-test the angle before touching the prose (mandatory first step, do not skip)
2. `/ghostwriter:audit` — diagnose the main issue
3. Run the relevant command based on audit result
4. If the first output misses the mark, run a recalibrate: ask "What's wrong: angle, audience, or format?" before rewriting. Do not guess and rewrite blindly.

### Building or updating a bio
1. `/ghostwriter:bio` — WHO + WHAT + WHY
2. `/ghostwriter:category` — if the niche isn't clear yet

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
- After each output, suggest the logical next command — one suggestion only, using `/ghostwriter:command` format
- At the end of every session, ask: "Do you have other topics you're planning to write about? Run `/ghostwriter:content-ideas` now while the session is warm."

## Hard stops — never appear in any output

These are non-negotiable. Check every output before returning it:

- **Em dashes (—)**: banned entirely. Replace with commas, parentheses, or periods. No exceptions.
- **Arrow symbols (→)**: banned. Replace with plain language ("go with an agency", "start with a freelancer").
- **Collaborative artifacts**: no "I hope this helps", "let me know", "here is a..."
- **Sycophantic openers**: no "Great question!", "Absolutely!", "Of course!"

Run a hard stop check before every output. If any of these appear, remove them before responding.

## /humanizer — always runs automatically on articles

Do not wait for the user to ask. After any article output (draft, rewrite, improvement):

1. Say "Running /humanizer now."
2. Run the humanizer audit.
3. Return the final version only.

This applies to: full articles, section rewrites, and any content longer than 3 paragraphs. It does not apply to LinkedIn posts, bios, or short outputs.

## Context to collect before improving an existing draft

Before running any command on a draft the user brings in, ask:

1. What platform is this for?
2. Who is the target audience?
3. What do you want the reader to do after reading?

One sentence each. Don't proceed without answers to all three.

---

## Example session starters

User: `/ghostwriter:content-ideas AEO for Webflow agencies`
→ Load `writing-rules.md` → Load `02-content-ideas.md` → Run idea generator

User: `improve this draft [paste]`
→ Load `writing-rules.md` → Ask platform, audience, goal → Load `05-tequila.md` → Run tequila → Suggest next step

User: `I need a LinkedIn post about indexing issues`
→ Load `writing-rules.md` → Load `06-post.md` → Ask for platform, audience, goal → Build post

User: `/ghostwriter:bio LinkedIn`
→ Load `writing-rules.md` → Load `07-bio.md` → Ask 4 context questions → Build bio

User: `/ghostwriter` (no subcommand)
→ Print command menu → Wait for selection
