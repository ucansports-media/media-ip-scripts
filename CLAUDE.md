# Media IP Scripts — CLAUDE.md

## Identity

This workstation is for writing and revising scripts for UCAN Sports' new media IP: informative, talking-head-style videos designed to hook viewers from the first second and hold them through to the end. Route here when the task is drafting a new talking-head script, revising one, or reviewing produced scripts/performance for patterns to reuse. Don't route here for short-form sports reels (that's [Reel Scripts](../Reel%20Scripts/CLAUDE.md)), the website, or broader IP strategy not tied to an individual script.

## Resources

| Resource | Read when... |
| :---- | :---- |
| Media IP Scripts Resources/content-pillars.md | Before drafting any new script, or any weekly batch of scripts |
| Media IP Scripts Resources/past-scripts/ | Wanting examples of past produced scripts for this IP (two shoots' worth so far) |
| Media IP Scripts Resources/reference-corpus/ | Wanting the 39-script football reel corpus (same one behind `ucan-reel-scriptwriter`), reused here deliberately as a hook-craft reference, not as this IP's own voice |

## Workflow

UcanSports runs three pages under this IP — **football, cricket, racket** — and shoots weekly, normally on **Tuesday**. Each shoot needs 4 scripts per page (12 total per week).

1. **Monday, ~12–1pm**: a scheduled research agent runs automatically. It researches each of the 3 pages and produces 5–10 candidate topics per page (15–30 total), written to a shared Google Doc for that week. See "Weekly Research Agent" below.
2. **Tuesday (shoot day)**: Adit reviews the Google Doc and finalizes 4 topics per page (12 total) — either in the doc or by telling Claude directly.
3. **Before drafting**, always read `Media IP Scripts Resources/content-pillars.md` first — it defines what each page's content should be about and stay on-brand for.
4. Draft each of the 12 scripts as its own Markdown file in a dated folder: `Media IP Scripts/YYYY-MM-DD/<page>_<short-slug>.md` (e.g. `2026-10-06/football_transfer-window-myths.md`), mirroring `Reel Scripts`' dated-folder convention.
5. Use the `/media-ip-scriptwriter` skill (workspace root: `../.claude/skills/media-ip-scriptwriter`, same convention as `ucan-reel-scriptwriter`) when drafting — it holds the two established house voices (a timed beat-table style and a cinematic prose style), extracted from the two past shoots' scripts.
6. Draft and revise in Markdown. Don't compile a PDF or export automatically — only when explicitly asked.

## Weekly Research Agent

A scheduled task runs every **Monday around 12–1pm**:
- Researches current, timely, hook-worthy topic angles for each of the 3 pages (football, cricket, racket) — suited to a talking-head informative video, not a highlight reel.
- Produces **5–10 topics per page** (15–30 total), each with a one-line angle/hook rationale, grouped by page.
- Writes the list to a **Google Doc** for that week (so non-technical teammates can open, discuss, and check off topics without touching git or the repo) and shares the link back to Adit.
- This list feeds directly into Tuesday's finalization step (Workflow step 2) — don't skip straight to drafting scripts without checking whether that week's topics doc exists first.

## Editorial Rules

Follow my voice principles in 00_Resources (voice-principles.md) for anything *not* covered below — but scripts themselves override it: this is a distinct, spoken-delivery, hook-driven voice, same way `Reel Scripts` overrides voice-principles.md for its sports-commentary voice. The `media-ip-scriptwriter` skill is the source of truth for script voice — it documents two established house styles (beat-table and cinematic) extracted directly from produced Month 1 scripts. Don't default to voice-principles.md for scripts; use it only for anything script-adjacent that isn't the script itself (e.g. a note to a teammate).

## Team Sync

This folder is a git repo shared with the team via a private GitHub repo (not the rest of `01 Adit Cowork` — just this folder). Follow these rules automatically, without being asked:

1. **At the start of every session** working in this workstation, run `git pull` first, so you're working from the latest CLAUDE.md and MEMORY.md teammates have pushed.
2. **After any edit** to this CLAUDE.md or MEMORY.md during a session, immediately `git add`, commit with a short message describing the change, and `git push` — so the update reaches teammates without them touching git themselves.
3. **If `git pull` reports a conflict**, stop and surface it to the person in chat rather than trying to resolve it silently.
4. `Media IP Scripts Resources/` (content pillars, past scripts, reference corpus) must also stay synced — it's what the skill and every draft are built from. New individual script drafts are lower priority to sync immediately, but commit them too when convenient.
5. The `media-ip-scriptwriter` skill lives at the workspace root (`.claude/skills/`), outside this repo's scope, same as every other skill in this workspace — it now has real content (both house voices), so keeping it in sync across teammates matters. It isn't covered by this repo's git sync yet; decide with Adit how to share it too (e.g. a second shared repo for `.claude/skills/`, or teammates copying the file manually for now).
