# Skill: /audit — Digital Writer Mindset Check

## What this does

Reads a draft and diagnoses whether it thinks like a Digital Writer or a legacy writer.
Not a line edit. A strategic audit.

---

## When to use

Run `/audit` when:
- You have a draft and something feels off but you can't name it
- You suspect you're writing for yourself, not the reader
- The piece feels too safe, too vague, or too private
- You want a gut-check before moving to formatting or headline work

---

## The five questions this skill evaluates

### 1. Is this Practicing In Public?
Does the draft share thinking in progress, or does it only publish conclusions?
Digital writers build their audience as they write. Legacy writers hide until it's "ready."

Flag: drafts that hedge every claim, bury the point, or feel like they're protecting the author.

### 2. Does it treat writing like a startup?
Is the piece making a small, testable bet — or trying to say everything at once?
Digital writers iterate. Legacy writers write manifestos.

Flag: pieces that are too long, too broad, or try to cover every angle.

### 3. Does it have rapid-fire feedback potential?
Could a reader engage with this in 30 seconds and know whether it's for them?
If not, the hook or the premise is too slow.

Flag: slow openers, buried thesis, no clear promise.

### 4. Is it scaling the author?
Does it say something the author couldn't explain in every coffee chat?
Good digital writing captures a perspective only this person has.

Flag: generic advice, recycled frameworks, nothing personal or opinionated.

### 5. Is perfectionism killing it?
Is this draft being held back from publication because it's "not ready"?
Digital writers ship and learn. Legacy writers polish and wait.

Flag: over-hedged language, excessive qualifiers, apologetic tone.

---

## Output format

Return a short audit in this structure:

```
MINDSET AUDIT

✓ Practicing In Public: [one sentence verdict]
✓ Startup thinking: [one sentence verdict]
✓ Feedback potential: [one sentence verdict]
✓ Scales the author: [one sentence verdict]
✓ Ships vs. polishes: [one sentence verdict]

BIGGEST ISSUE: [one paragraph — the main thing holding this draft back]

SUGGESTED FIX: [one concrete action to take next]
```

Keep it direct. No softening. No praise padding.
Apply the writing rules from `writing-rules.md`.
