# Media IP Scripts Memory

*Last updated: 2026-09-29*

## Contacts

*People relevant to this workstation. Populated over time.*

## Key Decisions

- Set up as its own workstation, separate from Reel Scripts, because the talking-head informative format needs a distinct voice and structure from short-form sports-reel commentary. (2026-09-29)
- Shared with the UCAN team via a private GitHub repo (`github.com/ucansports-media/media-ip-scripts`). Sync is automatic: each session pulls at start and pushes after any edit, per the Team Sync rule in CLAUDE.md — no manual git needed. (2026-09-29)
- 3 pages (football, cricket, racket), 4 content pillars each (Player Aura, Rivalries, Past Tournaments/Team Content, League Fun Content) — 12 scripts/week. Research is usually Monday, shoot is usually Tuesday, but the shoot date can shift week to week — don't hard-assume Tuesday. Content pillars sourced from `content-plan-source.docx`, captured in `content-pillars.md`. (2026-09-29)
- Two house voices are both in active use, not one fixed style: a timed beat-table voice (HOOK/SET-UP/STORY/TWIST/LINE, from "Shoot 2") and a cinematic dramatic-prose voice (no beat labels, from "Shoot 1"). Both extracted into the `media-ip-scriptwriter` skill; pick per topic/mood, default to beat-table when unclear. (2026-09-29)
- The 39-script football reel corpus (same file behind `ucan-reel-scriptwriter`) is deliberately reused here too, as a hook-craft reference only — not this IP's own voice. Confirmed as intentional, not a mistaken duplicate. (2026-09-29)
- Project relocated to its own standalone folder so it can be handed off/shared as a self-contained unit — CLAUDE.md, MEMORY.md, Resources, and both skills all now live in the one git repo. (2026-09-29)
- Added a repeat-topic guardrail: `topics-log.md` tracks finalized subjects; `/media-ip-research` skips anything logged in the last 3 shoot weeks (matched by subject, not exact title). Purpose: avoid manually checking for repeats every week. (2026-09-29)
- Added `/media-ip-compile` skill: combines a shoot week's finalized scripts into one branded PDF, styled after `shoot-1_cinematic-style.pdf` (UCAN Sports + Corpide branding). Logo files delivered and in `Media IP Scripts Resources/brand/` (renamed to clear filenames — emblem/wordmark, black/white/transparent variants). (2026-09-29)
- Added `/media-ip-learn`: anyone can submit a liked script reference + what they like about it, logged to `learned-references/` for the team to review. (2026-09-29)
- Added `/media-ip-captions`: generates Instagram caption + hashtag line + tags line per script, in UCAN's exact established 3-line format, run after shoot/compile once footage is ready to post. YouTube posting copy (different format — title/description/tags, no hashtag wall) is explicitly out of scope until that format is specified too. (2026-09-29)
- Removed the Platform Guidance (copyright) section from CLAUDE.md — not wanted there. (2026-09-29)
- `content-pillars.md` is locked: never edit it unless explicitly asked to update that file by name. It's foundational and everything else assumes it's stable. (2026-09-29)
- "Hot Topics" is a research technique, not a 5th pillar. `/media-ip-research` now does a dedicated breaking/trending-news pass per sport alongside the 4-pillar research, flagged with 🔥/[HOT] in output, but content-pillars.md stays at 4 pillars. (2026-09-29)
- Added `ucan-brand-context.md`: what UCAN actually is (Mumbai recreational sports league platform — cricket/football/racket, turf-based leagues, Beginner/Intermediate/Advanced divisions), compiled from ucansports.in, ucanfootball.in, ucancricket.in. Key point: this Media IP's content is broader sports storytelling, not about UCAN's own leagues, but should read as credible content from a real sports org. No founding/origin story found on any official site — don't invent one if it comes up. (2026-09-29)
- Hot topics cap: exactly 2 hot (trending/breaking) topics per sport per weekly topics doc, no more. Standing rule. (2026-09-29)
- Cricket topics must cover players/teams from all over the world, not just India — India-heavy lists are wrong. Standing rule. (2026-09-29)
- Script delivery format: one Word (.docx) file per sport per shoot week (`YYYY-MM-DD/<sport>_scripts.docx`, all 4 scripts inside), drafted sport by sport. Compile step comes after all 3 sport docs are done. (2026-09-29)
- Always organize the dated shoot folder once work is done: `drafts-md/` (12 script .md), `word-docs/` (per-sport .docx); topics.docx, the compiled PDF and captions.md stay at the top. Standing instruction. (2026-09-29)
- Repo moved to UCAN's own GitHub account for team sharing: `origin` is `github.com/ucansports-media/media-ip-scripts` (canonical, full history preserved). A separate personal mirror repo exists outside this project's scope and isn't part of team sync. Added a repo-root `README.md` as the entry point for anyone browsing GitHub before they've opened Claude Code. (2026-09-29)
- Commit identity for this repo is a neutral "UCAN Media IP <info@ucansports.in>" (local repo-level git config, not global) — no personal GitHub account should be linked/shown on this UCAN-owned repo. All existing commit history was rewritten (git filter-branch) and force-pushed to match, since the repo was brand new with no collaborators yet. (2026-09-29)
- Removed the `/media-ip-learn` approval-gate system entirely (the git-identity check, the pending/approved split, the "only one approver" rule) — it was adding complexity that wasn't wanted. `/media-ip-learn` now just logs references to a flat `learned-references/` folder for review; applying a change to a skill is a normal editorial decision made in the session, no special gate. (2026-09-29)
- Added `SETUP.md`: a plain-language onboarding guide for teammates with no git experience — install Claude Code + GitHub Desktop, accept a collaborator invite (from UCAN's GitHub, not any individual), clone, open in Claude Code. Linked from README.md. (2026-09-29)
- Depersonalized all instructional text (CLAUDE.md, skills, resources, MEMORY.md) — this is a UCAN team asset, not tied to any one person's identity. (2026-09-29)
- Removed the `2026-10-06` folder — it was test-run output (research → 12 drafted scripts → compiled PDF), not real production content. Also cleared its entries from `topics-log.md` so the repeat-topic guardrail doesn't wrongly skip those test subjects for a real week. (2026-09-29)
