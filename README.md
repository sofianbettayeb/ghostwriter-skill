# Ghostwriter

A writing skill for Claude Code. Made by Sofian Bettayeb.

Ghostwriter doesn't write for you. It gives you frameworks, asks better questions, and gets out of the way. The writing is still yours to do.

## Install

```bash
claude skill install gh:sofianbettayeb/ghostwriter-skill
```

Or locally:

```bash
git clone https://github.com/sofianbettayeb/ghostwriter-skill
claude skill install ./ghostwriter-skill
```

## Commands

| Command | What it does |
|---|---|
| `/audit` | Diagnoses a draft — are you writing for the reader, or for yourself? |
| `/content-ideas` | Four angles from a seed topic |
| `/headline` | Builds a headline and runs a curiosity gap test |
| `/format` | Checks skimmability, rhythm, and pacing |
| `/tequila` | Finds what makes the piece different — strips the clichés first |
| `/post` | LinkedIn post builder |
| `/bio` | WHO + WHAT + WHY for any platform |
| `/category` | Names and claims your content niche |

## Workflows

Each command loads a framework. You get a diagnosis or a structure, not a finished draft.

**Article from scratch:**
Run `/content-ideas` to find the angle, `/tequila` to check if it's actually different, `/headline` before you write a word, then `/format` once you have a draft.

**LinkedIn post:**
`/content-ideas` then `/post`.

**Improving a draft:**
Start with `/audit` to name the problem, then run whichever command fits.

**Bio:**
`/bio`, then `/category` if the niche still isn't clear.

## Writing rules

`writing-rules.md` is where you set your voice, constraints, and word blacklist. The skill loads it at the start of every session. For project-specific rules, duplicate and rename it — e.g., `writing-rules-myblog.md`.

## Files

```
ghostwriter-skill/
├── SKILL.md
├── writing-rules.md
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

---

Made by [Sofian Bettayeb](https://github.com/sofianbettayeb)
