End-of-session handoff - capture what matters from our conversation.
---
description: End-of-session summary
---

Synthesize this session into a handoff entry for `~/memory/.inbox.md`.

**Critical:** Only capture **reusable insights**, not one-off decisions.

## What to Capture

### Always Include:
- **Learnings:** Patterns, principles, or insights that apply beyond this specific task
  - Writing: Style insights, what worked/didn't work
  - Code: Architecture decisions, why X over Y
  - Research: Key findings, mental models
- **Technical Content:** New knowledge that should go in engineering files
- **Decisions with Rationale:** Only if the "why" is reusable

### Never Include UNLESS RELATED TO CODING:
- Specific edits ("moved section X to Y")
- Task completion status ("finished blog post")
- One-off decisions without broader insight
- Obvious next steps

## Format

```markdown
[YYYY-MM-DD HH:MM] Session: [Brief description]

Learnings:
- [Reusable insight with context]
- [Pattern or principle discovered]

Technical Content:
- [New knowledge for engineering files]

Decisions:
- [Decision + why it matters beyond this task]

Next:
- [Only non-obvious next steps]
```

## Examples

**Bad (too specific):**
```
Decisions:
- Move LPU section higher for early context
- Shorten conclusion from 17 to 6 lines
```

**Good (reusable insight):**
```
Learnings:
- Don't rehash in conclusions - tie forward, don't summarize backward
- Avoid jargon even in technical posts - "regulatory arbitrage" sounds corporate, not human
```

Append the handoff to `~/memory/.inbox.md`. Document WHAT WAS LEARNED, not just what files changed.
