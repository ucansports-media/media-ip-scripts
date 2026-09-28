---
name: media-ip-compile
description: "Compile a week's finalized talking-head scripts into a single shoot-day PDF, formatted in the cinematic house style (UCAN Sports + Corpide branding). Use when Adit runs /media-ip-compile, or asks to compile/print/export a week's scripts for shoot day."
---

# Media IP Compile

Combines all finalized scripts for one shoot week into a single branded PDF, mirroring the look of `Media IP Scripts Resources/past-scripts/shoot-1_cinematic-style.pdf` — that's the visual reference, regardless of which house voice (beat-table or cinematic) each individual script is written in.

## Steps

1. **Find the week**: if Adit names a date, use it; otherwise use the most recent dated folder at the project root (`YYYY-MM-DD/`). Confirm the date back if ambiguous.
2. **Collect scripts**: read every `<page>_<slug>.md` file in that dated folder. There should be up to 12 (4 pillars × 3 pages) — compile whatever's actually finalized, don't block on a partial week.
3. **Layout, matching the cinematic PDF reference**:
   - Header: UCAN Sports wordmark + Corpide logo (see Brand Assets below), "UCAN SPORTS · MEDIA IP" eyebrow label, orange accent rule.
   - Title: "Week of <date> — Shoot Scripts."
   - One section per pillar (Player Aura, Rivalries, Past Tournaments/Team Content, League Fun Content), scripts grouped under their pillar, in page order (football, cricket, racket) within each.
   - Per script: title, page/sport tag, pacing note if present, then the timed content — beat labels + VISUAL cues for beat-table-voice scripts, or the plain timed segments for cinematic-voice scripts. Match the two-column timestamp/visual-cue-then-line layout from the reference PDF where the script has that structure.
4. **Output**: `<that date>/YYYY-MM-DD_shoot-scripts.pdf` in the same dated folder, using the `pdf` (or `docx` → PDF) skill/toolchain.
5. **Commit and push** the PDF per the Team Sync rule.
6. **Only compile when explicitly asked** — never auto-generate this PDF as a side effect of drafting scripts.

## Brand Assets

Logos live in `Media IP Scripts Resources/brand/`. **This folder is currently empty** — Adit is sharing the UCAN Sports and Corpide logo files. Until they're added, build the PDF with clear placeholder logo boxes (labelled "UCAN SPORTS" / "CORPIDE") rather than blocking, and note in the output that placeholders were used. Once real logo files land in `brand/`, use them and drop the placeholder note.
