---
name: media-ip-research
description: "Research this week's script topics for UCAN's Media IP (football, cricket, racket) and write them to a Word doc for Tuesday's shoot. Use when Adit runs /media-ip-research, or asks for this week's topics, topic research, or the Monday research pass."
---

# Media IP Weekly Research Agent

Run this on demand (normally Monday) to produce candidate script topics for the upcoming Tuesday shoot.

## Steps

1. **Sync first**: run `git pull` at the project root, per the Team Sync rule in CLAUDE.md, so you're working from the latest shared state.
2. **Read context**: `Media IP Scripts Resources/content-pillars.md` (the 4 pillars) and `CLAUDE.md` (workflow, cadence) at the project root.
3. **Research**, using web search, current and timely angles for each of the 3 pages — **football, cricket, racket** — suited to a talking-head informative video (not a highlight reel — think storylines, records, rivalries, retrospectives, not "watch this clip"). Cover a spread across the 4 pillars (Player Aura, Rivalries, Past Tournaments/Team Content, League Fun Content) rather than clustering on one.
4. **Produce 5–10 topics per page** (15–30 total), grouped by page, each with:
   - A short working title
   - Which pillar it fits
   - A one-line angle/hook rationale — why this is worth a viewer's 45 seconds
5. **Find the upcoming Tuesday's date** (the next Tuesday from today, `YYYY-MM-DD`). Create that dated folder at the project root if it doesn't exist.
6. **Write the list to a Word doc** at `<that date>/topics.docx` (use the `docx` skill/toolchain to produce it — a clean doc with a page-by-page heading structure, easy for Adit to review and mark up on Tuesday).
7. **Commit and push**: `git add`, commit (e.g. "Add topics for <date> shoot"), and `git push` at the project root, per the Team Sync rule — this is what makes the doc show up for teammates too.
8. **Tell Adit** the doc is ready, with its path, and a quick one-line summary of the spread of topics (e.g. "6 football, 7 cricket, 5 racket, covering all 4 pillars").

## Notes

- This was originally planned as a fully automated Monday cloud schedule, but that needs GitHub connected to the Claude account for cloud access — not set up yet. Until/unless that changes, this runs on demand via `/media-ip-research` (or a direct request) instead of on a timer.
- Don't skip step 1 or step 7 — the whole point of writing to this project is that it syncs to teammates automatically; a topics doc that isn't pushed doesn't help anyone but Adit's local machine.
