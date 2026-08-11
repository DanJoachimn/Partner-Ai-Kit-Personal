---
type: folder-note
generated_by: claude-code
---

# Meetings/

Meeting notes — client calls, supplier quarterlies, collab discussions, podcast guest pre-calls.

## Naming convention

`YYYY-MM-DD — [who / what].md`

Examples:
- `2026-05-01 — [Brand] intro call.md`
- `2026-05-03 — Supplier quarterly.md`

## The AI's role

- **Read** freely.
- **Clean up raw transcripts on request.** [PARTNER_NAME] hands over a messy transcript, [[ops]] subagent pulls decisions + action items (see ops.md — hard rule: don't write show notes, that's content's job).
- **Append follow-up actions** when they say "add to the meeting note that I'll follow up with X."

## Format for processed meeting notes

```markdown
---
date: 2026-05-01
attendees:
  - [PARTNER_NAME]
  - [Other name]
type: meeting
generated_by: [AI_NAME]
---

# [Meeting title]

## Decisions made
- ...

## Action items
- [PARTNER_NAME] — [thing] — [deadline]
- [Other] — [thing] — [deadline]

## Notes / context
[Anything else worth keeping]
```

---

*Delete this README whenever.*
