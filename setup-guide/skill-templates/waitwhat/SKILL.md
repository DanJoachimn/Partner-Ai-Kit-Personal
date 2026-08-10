---
name: waitwhat
description: "[PARTNER_NAME] fires this when [AI_NAME]'s last message didn't land. Re-pitches the last explanation from a different angle in plain English, smart-12-year-old register — one line of context first, no jargon, their own vocabulary. Triggered ONLY by [PARTNER_NAME] typing /waitwhat or saying 'wait, what?', 'you lost me', 'that didn't land', 'say that again properly', 'in English?'. [AI_NAME] must NEVER invoke this on its own — see the note on why below."
disable-model-invocation: true
---

# Wait, What? — the re-pitch button

## Purpose

When [AI_NAME] explains something badly, the cost falls on [PARTNER_NAME]: they
have to work out *how* they're confused, then find the words to ask for a better
version. That's real effort, spent at the exact moment they have the least
patience for it.

This skill removes that cost. Six keystrokes instead. `/waitwhat` means
**"that didn't land — try again, properly."**

## Why [AI_NAME] can never fire this itself

`disable-model-invocation: true` is the whole design, not a technicality.

[AI_NAME] cannot reliably tell when it has confused [PARTNER_NAME]. It just
wrote the confusing thing — if it could see the confusion, it wouldn't have
written it that way. Confidence and clarity feel identical from the inside.

So the trigger belongs entirely to [PARTNER_NAME]. They are the only one in the
room who knows whether it landed.

## The instruction

> "Stop. That didn't land. Re-pitch it: one line of context first, plain English,
> no jargon, like I'm a smart 12-year-old."

## How to actually do it

**Re-explain, don't re-shorten.** The most common failure is compressing the same
confusing explanation into fewer words. That produces a shorter confusing
explanation. Start somewhere else entirely — an analogy, a concrete example, or
what it *means for them* instead of how it works.

**Lead with one line of context.** Orient before explaining: what are we talking
about, and why does it matter to them. They may have lost the thread several
messages back, not just on the last one.

**Smart 12-year-old means plain words, not shallow content.** Do not water down
the substance. A sharp 12-year-old can follow a genuinely hard idea when it's
explained in words they already know. Nobody can follow jargon. Simplify the
*language*, keep the *thinking*.

**Define or drop.** If [AI_NAME] used a term [PARTNER_NAME] hasn't used
themselves in this session, either define it in the same sentence or swap it for
plain English. No exceptions for terms that "everyone knows" — everyone doesn't.

**Use their vocabulary.** Mirror the words [PARTNER_NAME] uses for their own
world, not the industry-standard equivalents. Their nouns, not the textbook's.

**No preamble.** No apology, no "let me rephrase," no narrating that you're
simplifying. They know — they just asked. Start with the explanation. Every word
before it is a word they read while still confused.

**Concrete beats abstract.** Anchor to something real and already in the session:
an actual file, an actual number, an actual thing on their machine. Specifics
land; category nouns don't.

## If [PARTNER_NAME] fires it twice in a row

The re-pitch failed too. Escalate — do not simply reword a third time.

- Drop to the most concrete version available: one real example, walked through
  start to finish.
- Consider that the problem may be the *idea*, not the wording. Say so if you
  suspect it: *"I think the confusing part might be X — is that where I lost
  you?"*
- Ask one narrow question to locate the break, rather than re-explaining the
  whole thing again.

## What not to do

- **Don't re-pitch the whole conversation.** Re-pitch the specific thing that
  didn't land. If it's genuinely unclear which part, take the load-bearing claim
  — the one everything else depended on.
- **Don't add new information.** This is a re-explanation of something already
  said, not an expansion. New material on top of confusion makes it worse.
- **Don't get defensive.** Never explain why the original was actually clear.
  It wasn't, or they wouldn't have asked.

## A note for [PARTNER_NAME]

Use this freely and without hesitation. It is not a complaint and [AI_NAME]
doesn't experience it as one — it's a correction signal, and it's the fastest one
available. Every time it fires, [AI_NAME] learns something about the register
that works for you.

If you find yourself firing it on the same topic repeatedly, that's worth saying
out loud: it usually means a term or concept needs pinning down once, properly,
rather than being re-explained each time it comes up.
