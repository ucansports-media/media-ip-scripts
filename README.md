# UCAN Media IP — Scriptwriter Agent

A self-contained Claude Code project that writes, researches, compiles, and captions scripts for UCAN Sports' talking-head Media IP (football, cricket, racket sports).

## What this is

UCAN's Media IP produces short informative talking-head videos, 12 a week (4 topics × 3 pages — football, cricket, racket). This project is the agent that runs that pipeline: weekly topic research, script drafting in UCAN's established house voice, shoot-day PDF compilation, and Instagram caption generation — all through Claude Code.

## Getting started

1. **Install [Claude Code](https://claude.com/claude-code)** if you don't already have it.
2. **Clone this repo** to your machine (GitHub Desktop is the easiest way if you're not comfortable with git commands: File → Clone Repository → paste this repo's URL).
3. **Open the cloned folder in Claude Code.** Everything else is automatic from there — Claude reads [`CLAUDE.md`](CLAUDE.md) at the start of every session, which explains the full workflow, and pulls the latest shared state automatically.

## The weekly cycle, in short

| Step | Command | What it does |
| :---- | :---- | :---- |
| 1. Research | `/media-ip-research` | Researches topics for football/cricket/racket, writes `topics.docx` for that week |
| 2. Finalize | *(just tell Claude)* | You pick 4 topics per page; Claude logs them so they don't repeat |
| 3. Draft | `/media-ip-scriptwriter` | Writes the 12 scripts in UCAN's established voice |
| 4. Compile | `/media-ip-compile` | Combines the week's scripts into one branded shoot-day PDF |
| 5. Caption | `/media-ip-captions` | Generates Instagram caption/hashtag/tag copy once footage is ready to post |

Anyone can also run `/media-ip-learn` at any time to submit a script reference they liked — it's queued for review, not applied automatically.

Full details, rules, and the reasoning behind them live in [`CLAUDE.md`](CLAUDE.md). Decision history is in [`MEMORY.md`](MEMORY.md).

## Working as a team

This repo is the single source of truth — `CLAUDE.md`, `MEMORY.md`, resources, and every skill all live here together, so cloning this repo gets you the whole agent. Claude Code pulls automatically at the start of every session and pushes after edits, so staying in sync doesn't take any manual git work. See the **Team Sync** section in `CLAUDE.md` for the exact rules.
