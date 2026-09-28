# Media IP Scripts Memory

*Last updated: 2026-09-29*

## Contacts

*People relevant to this workstation. Populated over time.*

## Key Decisions

- Set up as its own workstation, separate from Reel Scripts, because the talking-head informative format needs a distinct voice and structure from short-form sports-reel commentary. (2026-09-29)
- Shared with 2-3 teammates via a private GitHub repo (`github.com/editsbyadit/media-ip-scripts`). Sync is automatic: each teammate's Claude Code session pulls at session start and pushes after any edit, per the Team Sync rule in CLAUDE.md — no manual git needed from teammates. (2026-09-29)
- 3 pages (football, cricket, racket), 4 content pillars each (Player Aura, Rivalries, Past Tournaments/Team Content, League Fun Content) — 12 scripts/week. Research is usually Monday, shoot is usually Tuesday, but the shoot date can shift week to week — don't hard-assume Tuesday. Content pillars sourced from `content-plan-source.docx`, captured in `content-pillars.md`. (2026-09-29)
- Two house voices are both in active use, not one fixed style: a timed beat-table voice (HOOK/SET-UP/STORY/TWIST/LINE, from "Shoot 2") and a cinematic dramatic-prose voice (no beat labels, from "Shoot 1"). Both extracted into the `media-ip-scriptwriter` skill; pick per topic/mood, default to beat-table when unclear. (2026-09-29)
- The 39-script football reel corpus (same file behind `ucan-reel-scriptwriter`) is deliberately reused here too, as a hook-craft reference only — not this IP's own voice. Confirmed by Adit as intentional, not a mistaken duplicate. (2026-09-29)
- Project relocated from inside `01 Adit Cowork` to its own standalone folder (`C:\Users\adity\Desktop\Media IP Scripts`) so it can be handed off/shared as a self-contained unit — CLAUDE.md, MEMORY.md, Resources, and both skills all now live in the one git repo. (2026-09-29)
- Added a repeat-topic guardrail: `topics-log.md` tracks finalized subjects; `/media-ip-research` skips anything logged in the last 3 shoot weeks (matched by subject, not exact title). Adit wanted this specifically to avoid manually checking for repeats every week. (2026-09-29)
- Added `/media-ip-compile` skill: combines a shoot week's finalized scripts into one branded PDF, styled after `shoot-1_cinematic-style.pdf` (UCAN Sports + Corpide branding). Logo files delivered and in `Media IP Scripts Resources/brand/` (renamed to clear filenames — emblem/wordmark, black/white/transparent variants). (2026-09-29)
- Added `/media-ip-learn`: anyone can submit a liked script reference + what they like about it, but it only ever queues to `learned-references/pending/` — applying it to a skill or CLAUDE.md requires Adit's explicit approval (identity check via `git config user.email == editsbyadit@gmail.com`, plus an explicit yes/no confirmation even when that matches). Adit's own rationale: teammates might submit weaker references that could dilute the house voice if applied automatically — this is a deliberate guardrail, not a reflection of distrust. (2026-09-29)
- Added `/media-ip-captions`: generates Instagram caption + hashtag line + tags line per script, in Adit's exact established 3-line format, run after shoot/compile once footage is ready to post. YouTube posting copy (different format — title/description/tags, no hashtag wall) is explicitly out of scope until Adit gives that format too. (2026-09-29)
- Open question, not yet decided: a formal copyright/rights-sourcing policy for footage and music across Instagram vs. YouTube. General guidance captured in CLAUDE.md's Platform Guidance section; no firm rule yet on footage sourcing (broadcast clips vs. original/licensed) or music licensing. (2026-09-29)
