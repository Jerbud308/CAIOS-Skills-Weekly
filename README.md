# CAIOS Skills Weekly

A RAC Projects AI production. A weekly job that publishes one "steal this" GitHub repo or tool breakdown, written for the AITP Skool community: consultants and AI transformation partners, not developers.

## What this does

Every Monday at 08:00 AM, a ClaudeClaw scheduled task (`bb0fece4`, `node dist/schedule-cli.js list` from the claudeclaw repo to inspect it) clones/pulls this repo and runs the instructions in [`ROUTINE.md`](./ROUTINE.md).

The real queue lives in Obsidian, not in this repo: `02-Projects/RAC Projects AI/Research/GitHub Repos Worth Sharing.md` holds 500+ candidate repos pulled from Jeremy's daily trending-repos digest, organized by category. Jeremy checks a box on ones he's actually used or genuinely vouches for. Each week the routine picks the first checked-and-unposted repo, reads its real README (not just the digest's one-line take), writes a Skool-ready post, and marks that line `(posted DATE)` in the Obsidian note so it isn't picked again.

If nothing's checked yet, it's a **fallback week**: the routine picks its own best candidate from the latest trending digest and says so plainly at the top of the post, it's explicitly flagged as not-yet-approved, and the footer drops the "built and used" claim since nobody's vetted it. Check its box in Obsidian (or check a different one) if you're good with it.

Jeremy's own built skills (`inputs/skills-queue.md`) are still in the mix, but only as an occasional, manually-triggered one-off, never the automatic weekly pick, per feedback that a whole series built on internal skills read weak once genericized.

It commits the result to [`outputs/`](./outputs/) and sends Jeremy a short Telegram ping pointing at the dashboard, it does not dump the draft into chat.

It never posts to Skool itself. Jeremy reads and copies the draft from the dashboard, edits if needed, ships it.

## How it's wired

This runs on the ClaudeClaw bot's own scheduler, not a hosted Claude Code Routine, so there's no separate web UI to maintain. See `docs/solutions/` in the claudeclaw repo (`orphaned-cron-prompt-scheduled-tasks-2026-07-02.md`) for why recurring work in that project always goes through the local scheduler. To change the schedule or the wrapper prompt, edit task `bb0fece4` via the `schedule` skill; to change what the routine actually does, edit `ROUTINE.md` in this repo, the scheduler prompt just points at it.

## How to read the output

- **Dashboard (primary):** Mission Control → Skills Weekly (`/skills-weekly`, shortcut `g k`) reads every file in `outputs/` on Jeremy's Mac and renders them as a scrollable feed, newest first, each with a one-click copy button. Backend route: `src/dashboard/routes/skills-weekly.ts` in the claudeclaw repo.
- `outputs/caios-skill-<slug>-YYYY-MM-DD.md`, that week's post, ready to paste into Skool
- Each file is append-only (the routine never modifies past runs)
- Git history = your archive of every post you've shipped

## How to tune

- Approve a repo for next Monday → check its box in the Obsidian note
- Change voice, audience, or genericization rules → edit [`.claude/CLAUDE.md`](./.claude/CLAUDE.md)
- Change the post format or sourcing logic itself → edit [`ROUTINE.md`](./ROUTINE.md)
- Cover one of Jeremy's own skills instead → ask for that explicitly, it isn't automatic

## Kill date

Review once the Obsidian candidate pool runs low on unchecked repos, or if fallback weeks (unapproved picks) start outnumbering approved ones, that's a signal the checkbox habit isn't sticking and the process needs rethinking.
