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

Type `/ghostwriter` with no subcommand to see the full menu. Or jump straight to a command:

| Command | What it does |
|---|---|
| `/ghostwriter:audit` | Diagnoses a draft — are you writing for the reader, or for yourself? |
| `/ghostwriter:content-ideas` | Four angles from a seed topic |
| `/ghostwriter:headline` | Builds a headline and runs a curiosity gap test |
| `/ghostwriter:format` | Checks skimmability, rhythm, and pacing |
| `/ghostwriter:tequila` | Finds what makes the piece different — strips the clichés first |
| `/ghostwriter:post` | LinkedIn post builder |
| `/ghostwriter:bio` | WHO + WHAT + WHY for any platform |
| `/ghostwriter:category` | Names and claims your content niche |

## Workflows

Each command loads a framework. You get a diagnosis or a structure, not a finished draft.

**Article from scratch:**
Run `/ghostwriter:content-ideas` to find the angle, `/ghostwriter:tequila` to check if it's actually different, `/ghostwriter:headline` before you write a word, then `/ghostwriter:format` once you have a draft.

**LinkedIn post:**
`/ghostwriter:content-ideas` then `/ghostwriter:post`.

**Improving a draft:**
Start with `/ghostwriter:tequila` to pressure-test the angle, then `/ghostwriter:audit` to name the problem, then run whichever command fits.

**Bio:**
`/ghostwriter:bio`, then `/ghostwriter:category` if the niche still isn't clear.

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
