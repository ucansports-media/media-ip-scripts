# Media IP Scripts — CLAUDE.md

## Identity

This is a standalone Claude Code project for UCAN Sports' Media IP: informative, talking-head-style videos designed to hook viewers from the first second and hold them through to the end. Route here for drafting a new talking-head script, revising one, or reviewing produced scripts/performance for patterns to reuse. This project is self-contained (its own CLAUDE.md, MEMORY.md, resources, and skills) so it can be shared or handed off as a unit. It does not cover UCAN's short-form sports reels (a separate "Reel Scripts" workstation elsewhere), the website, or broader IP strategy not tied to an individual script.

## Resources

| Resource | Read when... |
| :---- | :---- |
| Media IP Scripts Resources/content-pillars.md | Before drafting any new script, or any weekly batch of scripts |
| Media IP Scripts Resources/past-scripts/ | Wanting examples of past produced scripts for this IP (two shoots' worth so far) |
| Media IP Scripts Resources/reference-corpus/ | Wanting the 39-script football reel corpus (same one behind `ucan-reel-scriptwriter`), reused here deliberately as a hook-craft reference, not as this IP's own voice |
| Media IP Scripts Resources/topics-log.md | Before suggesting new topics (avoid repeats) and after finalizing a week's topics (log them) |
| Media IP Scripts Resources/brand/ | Compiling a shoot-day PDF — holds the UCAN Sports and Corpide logo files |

## Workflow

UcanSports runs three pages under this IP — **football, cricket, racket** — and shoots roughly weekly. Research usually happens Monday and the shoot is usually Tuesday, but the shoot date can shift week to week — don't hard-assume Tuesday, ask or check the dated folder if unclear. Each shoot needs 4 scripts per page (12 total per week).

1. **Research day (usually Monday)**: run `/media-ip-research` to research topics. It checks `topics-log.md` to avoid recent repeats, then produces 5–10 candidate topics per page (15–30 total), written to a Word doc for that week's shoot. See "Weekly Research Agent" below.
2. **Shoot day (usually Tuesday)**: Adit reviews the topics doc and finalizes 4 topics per page (12 total) — either by editing the doc or by telling Claude directly. **Log the 4x3 finalized subjects to `Media IP Scripts Resources/topics-log.md`** at this point (date, page, pillar, subject, script title) — this is what makes the repeat-topic guardrail work.
3. **Before drafting**, always read `Media IP Scripts Resources/content-pillars.md` first — it defines what each page's content should be about and stay on-brand for.
4. Draft each of the 12 scripts as its own Markdown file in a dated folder: `YYYY-MM-DD/<page>_<short-slug>.md` (e.g. `2026-10-06/football_transfer-window-myths.md`) at the project root.
5. Use the `/media-ip-scriptwriter` skill (`.claude/skills/media-ip-scriptwriter`) when drafting — it holds the two established house voices (a timed beat-table style and a cinematic prose style), extracted from the two past shoots' scripts.
6. Draft and revise in Markdown. Don't compile a PDF or export automatically — only when explicitly asked. When asked, use the `/media-ip-compile` skill (`.claude/skills/media-ip-compile`) to combine the week's scripts into one branded shoot-day PDF.

## Weekly Research Agent

Run via the `/media-ip-research` skill (`.claude/skills/media-ip-research`), on demand — usually Monday, but whenever Adit chooses to run it:
- Checks `Media IP Scripts Resources/topics-log.md` and skips any subject used in the last 3 shoot weeks.
- Researches current, timely, hook-worthy topic angles for each of the 3 pages (football, cricket, racket) — suited to a talking-head informative video, not a highlight reel.
- Produces **5–10 topics per page** (15–30 total), each with a one-line angle/hook rationale, grouped by page.
- Writes the list to a **Word doc** (.docx) at `YYYY-MM-DD/topics.docx` (project root), where `YYYY-MM-DD` is that week's upcoming shoot date (create the dated folder if it doesn't exist yet), then commits and pushes it — so it's git-synced to the team automatically via the normal Team Sync rule.
- This list feeds directly into the shoot-day finalization step (Workflow step 2) — don't skip straight to drafting scripts without checking whether that week's `topics.docx` exists first.

**Note:** this was originally planned as a fully automatic Monday cloud schedule, but that needs GitHub connected to Adit's Claude account for cloud access (separate from the local `gh` login already set up) — not done yet. Runs on demand for now via `/media-ip-research`; revisit a real schedule once that's connected, if still wanted.

## Editorial Rules

This project's scripts have their own established voice — the `media-ip-scriptwriter` skill is the source of truth for it, documenting two house styles (beat-table and cinematic) extracted directly from produced Month 1 scripts. This project doesn't depend on any external voice-principles file; it's meant to be self-contained. Use the skill for scripts; use plain, direct, professional writing for anything script-adjacent that isn't the script itself (e.g. a note to a teammate).

## Team Sync

This entire project (CLAUDE.md, MEMORY.md, Resources, and `.claude/skills/`) is one git repo shared with the team via a private GitHub repo. Everything needed to work on this IP lives inside this one repo — that's deliberate, so it can be cloned or handed off as a self-contained unit. Follow these rules automatically, without being asked:

1. **At the start of every session** working in this project, run `git pull` first, so you're working from the latest CLAUDE.md, MEMORY.md, Resources, and skills teammates have pushed.
2. **After any edit** to CLAUDE.md, MEMORY.md, Resources, or a skill file during a session, immediately `git add`, commit with a short message describing the change, and `git push` — so the update reaches teammates without them touching git themselves.
3. **If `git pull` reports a conflict**, stop and surface it to the person in chat rather than trying to resolve it silently.
4. New individual script drafts are lower priority to sync immediately, but commit them too when convenient.
