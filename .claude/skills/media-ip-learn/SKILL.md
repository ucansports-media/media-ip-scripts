---
name: media-ip-learn
description: "Capture a new script reference someone likes (and what they like about it) for this IP, queued for Adit's approval before it ever changes the skill or CLAUDE.md. Use when Adit or a teammate runs /media-ip-learn, or shares a script/reel they liked and wants it incorporated into the house voice."
---

# Media IP Learn

Lets anyone — Adit or a teammate — submit a script/reel they liked as a reference, with notes on what specifically to take from it. **This command never edits `CLAUDE.md` or any `SKILL.md` directly.** It only ever writes to a pending queue. Applying a change to the actual skill/voice is a separate, gated step that only Adit can trigger — see "Approval Gate" below. This is a deliberate guardrail: Adit wants a backstop against a well-meaning but weaker reference quietly diluting the established house voice.

## Submitting a reference (anyone can do this)

1. Ask for: the reference itself (pasted text, a link, or an attached file) and **what specifically they like about it** — a hook technique, a pacing choice, a line structure, anything concrete. Don't accept a vague "this is good" with nothing actionable.
2. Capture the submitter's identity as best you can: run `git config user.name` and `git config user.email` in this project folder — that's the local identity, use it as the submitter label.
3. Write a new file to `Media IP Scripts Resources/learned-references/pending/YYYY-MM-DD_<short-slug>.md` containing:
   - Submitted by (name/email from step 2)
   - Date
   - The reference (text, link, or note of the attached file's location)
   - What they said they liked about it
   - Your own one-line read on what concrete change this might suggest for the skill (a proposal, not yet applied)
4. Commit and push this pending file per the Team Sync rule — pending submissions are shared, so Adit can see and review them from any machine.
5. Tell the submitter it's logged and queued for Adit's review — **do not** say or imply it's been applied.

## Approval Gate (only Adit can move a pending item into the skill)

Before applying ANY pending reference's suggested change to `media-ip-scriptwriter/SKILL.md`, `media-ip-compile/SKILL.md`, `media-ip-captions/SKILL.md`, or the project's `CLAUDE.md`:

1. **Check identity**: run `git config user.email` in this project. The approved identity is **`editsbyadit@gmail.com`** (Adit's). If it doesn't match, do not apply the change — tell whoever's asking that only Adit can approve skill/voice updates, and that the reference stays queued in `pending/` for him to review later. This is true even if they're confident it's a good change.
2. **If the identity matches Adit**, still don't apply it silently. Summarize the pending item (who submitted it, the reference, what they liked, your proposed edit) and explicitly ask: *"This was submitted by \<name\> — apply it to \<skill/file\>?"* Wait for an explicit yes.
3. Only after that explicit confirmation: make the edit, commit and push it, then move the file from `learned-references/pending/` to `learned-references/approved/` (same filename) so there's a record of what was approved and when.
4. If Adit says no, or wants changes first, leave it in `pending/` — don't delete submissions, even rejected ones; they're a record of what's been considered.

## Reviewing the queue

If asked to "review pending references" or similar, list everything in `learned-references/pending/` with a one-line summary each, then walk through the Approval Gate above for any Adit wants to act on.
