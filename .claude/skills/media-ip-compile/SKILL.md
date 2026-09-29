---
name: media-ip-compile
description: "Compile a week's finalized talking-head scripts into a single shoot-day PDF, formatted in the cinematic house style (UCAN Sports + Corpide branding). Use when Adit runs /media-ip-compile, or asks to compile/print/export a week's scripts for shoot day."
---

# Media IP Compile

Combines all finalized scripts for one shoot week into a single branded PDF, mirroring the look of `Media IP Scripts Resources/past-scripts/shoot-1_cinematic-style.pdf` — that's the visual reference, regardless of which house voice (beat-table or cinematic) each individual script is written in.

## Steps

1. **Find the week**: if Adit names a date, use it; otherwise use the most recent dated folder at the project root (`YYYY-MM-DD/`). Confirm the date back if ambiguous.
2. **Collect scripts**: read every `<page>_<slug>.md` file in that dated folder's `drafts-md/` subfolder (or the folder itself for older weeks). There should be up to 12 (4 pillars × 3 pages) — compile whatever's actually finalized, don't block on a partial week.
3. **Layout, matching the cinematic PDF reference**:
   - Header: UCAN Sports wordmark + Corpide logo (see Brand Assets below), "UCAN SPORTS · MEDIA IP" eyebrow label, orange accent rule.
   - Title: "Week of <date> — Shoot Scripts."
   - One section per pillar (Player Aura, Rivalries, Past Tournaments/Team Content, League Fun Content), scripts grouped under their pillar, in page order (football, cricket, racket) within each.
   - Per script: title, page/sport tag, pacing note if present, then the timed content — beat labels + VISUAL cues for beat-table-voice scripts, or the plain timed segments for cinematic-voice scripts. Match the two-column timestamp/visual-cue-then-line layout from the reference PDF where the script has that structure.
4. **Output**: `<that date>/YYYY-MM-DD_shoot-scripts.pdf` in the same dated folder, using the `pdf` (or `docx` → PDF) skill/toolchain.
5. **Commit and push** the PDF per the Team Sync rule.
6. **Only compile when explicitly asked** — never auto-generate this PDF as a side effect of drafting scripts.

## Brand Assets

Logos live in `Media IP Scripts Resources/brand/`:
- `ucan-sports-emblem-black.png` / `ucan-sports-emblem-white.png` — UCAN Sports emblem, pick by background (white background → black emblem, dark background → white emblem).
- `corpide-emblem.png` / `corpide-emblem-transparent.png` — Corpide emblem (the transparent version for overlaying on a colored/textured header).
- `corpide-wordmark-black.png` / `corpide-wordmark-white.png` — Corpide text logo, pick by background same as above.

Match the reference PDF's header layout: UCAN Sports emblem + "UCAN SPORTS · MEDIA IP" eyebrow text on one side, Corpide mark (emblem or wordmark, whichever reads cleaner at header size) on the other, orange accent rule beneath.
