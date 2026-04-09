# Ghostwriter Skill for Claude Code

A writing system built on 8 frameworks from Ship 30 for 30. Edit and improvement focused — not a content generator. Works on articles, LinkedIn posts, and bios.

## Install

```bash
claude skill install gh:your-username/ghostwriter-skill
```

Or clone and install locally:

```bash
git clone https://github.com/your-username/ghostwriter-skill
claude skill install ./ghostwriter-skill
```

## Commands

| Command | What it does |
|---|---|
| `/audit` | Diagnoses a draft — digital writer vs legacy writer mindset |
| `/content-ideas` | Generates 4 content angles from a seed topic |
| `/headline` | Builds a 5-piece headline and runs a curiosity gap test |
| `/format` | Checks skimmability, rhythm, and rate of revelation |
| `/tequila` | Strips the clichés — finds what makes the piece actually different |
| `/post` | Builds a LinkedIn post using a 12-strategy framework |
| `/bio` | WHO + WHAT + WHY bio builder for any platform |
| `/category` | Names and claims your content niche |

## Workflows

**Write an article from scratch**
1. `/content-ideas [topic]` — find the angle
2. `/tequila` — make sure it's differentiated
3. `/headline` — nail the title before writing
4. Write the draft
5. `/format` — structure and rhythm check

**Write a LinkedIn post**
1. `/content-ideas [topic]` — find the angle
2. `/post` — build the post

**Improve an existing draft**
1. `/audit` — diagnose the main issue
2. Run the relevant command based on audit result

**Build or update a bio**
1. `/bio` — WHO + WHAT + WHY
2. `/category` — if the niche isn't clear yet

## Customize your writing rules

Edit `writing-rules.md` to set your voice, style constraints, and word blacklist. The skill loads this file at the start of every session.

For project-specific rules, duplicate and rename it (e.g., `writing-rules-myblog.md`) and reference it when triggering the skill.

## File structure

```
ghostwriter-skill/
├── SKILL.md              # Skill definition and command routing
├── writing-rules.md      # Voice, style, and word rules (edit this)
└── skills/
    ├── 01-audit.md
    ├── 02-content-ideas.md
    ├── 03-headline.md
    ├── 04-format.md
    ├── 05-tequila.md
    ├── 06-post.md
    ├── 07-bio.md
    └── 08-category.md
```

## Trigger phrases

Beyond slash commands, the skill activates on natural language like:
- "help me write a LinkedIn post"
- "give me content ideas about X"
- "improve this draft"
- "write my bio"
- "what should I write about"
