# Media IP Scripts — CLAUDE.md

## Identity

This workstation is for writing and revising scripts for UCAN Sports' new media IP: informative, talking-head-style videos designed to hook viewers from the first second and hold them through to the end. Route here when the task is drafting a new talking-head script, revising one, or reviewing produced scripts/performance for patterns to reuse. Don't route here for short-form sports reels (that's [Reel Scripts](../Reel%20Scripts/CLAUDE.md)), the website, or broader IP strategy not tied to an individual script.

## Resources

| Resource | Read when... |
| :---- | :---- |
| *(none yet — add example scripts, performance data, or style references here as they're gathered)* | |

## Workflow

1. When starting work on a new talking-head script, draft it as its own Markdown file. Organize scripts by topic or shoot date (confirm which fits better with Adit once volume picks up — mirror `Reel Scripts`' dated-folder pattern if useful).
2. Use the `/media-ip-scriptwriter` skill (workspace root: `../.claude/skills/media-ip-scriptwriter`, same convention as `ucan-reel-scriptwriter`) when drafting, once it's built out — it will hold the hook formula, structure, and voice for this IP.
3. Draft and revise in Markdown. Don't compile a PDF or export automatically — only when explicitly asked.

**Note:** This skill is not yet built. The hook/structure/voice patterns for this IP need to be developed — either by analyzing example scripts once some exist, or by iterating live with Adit script by script. Until then, draft using the Editorial Rules below and Adit's direct feedback.

## Editorial Rules

Follow my voice principles in 00_Resources (voice-principles.md) — but note: talking-head informative scripts are likely a distinct voice (built for spoken delivery, hook-driven, retention-optimized) that won't map cleanly onto Adit's personal/email voice, the same way `Reel Scripts` overrides voice-principles.md for its sports-commentary voice. Once a clear pattern emerges from produced scripts, capture it here (or in the skill) rather than defaulting to voice-principles.md for every draft.

## Team Sync

This folder is a git repo shared with the team via a private GitHub repo (not the rest of `01 Adit Cowork` — just this folder). Follow these rules automatically, without being asked:

1. **At the start of every session** working in this workstation, run `git pull` first, so you're working from the latest CLAUDE.md and MEMORY.md teammates have pushed.
2. **After any edit** to this CLAUDE.md or MEMORY.md during a session, immediately `git add`, commit with a short message describing the change, and `git push` — so the update reaches teammates without them touching git themselves.
3. **If `git pull` reports a conflict**, stop and surface it to the person in chat rather than trying to resolve it silently.
4. New script drafts under this folder can be committed too, but syncing script drafts isn't the priority — CLAUDE.md and MEMORY.md are what must always stay current across teammates.
5. The `media-ip-scriptwriter` skill lives at the workspace root (`.claude/skills/`), outside this repo's scope, same as every other skill in this workspace. It's an empty placeholder for now, so this isn't urgent — once it's built out, decide with Adit how to keep it synced across teammates too (e.g. pulling it into this same repo, or a second shared location).
