# CAIOS Skills Weekly

A RAC Projects AI production. A weekly job that publishes one "steal this" AI skill breakdown, written for the AITP Skool community: consultants and AI transformation partners, not developers.

## What this does

Every Monday at 08:00 AM, a ClaudeClaw scheduled task (`bb0fece4`, `node dist/schedule-cli.js list` from the claudeclaw repo to inspect it) clones/pulls this repo and runs the instructions in [`ROUTINE.md`](./ROUTINE.md). It picks the next skill from the queue, reads the real SKILL.md behind it on Jeremy's Mac, and writes a Skool-ready post: what it is, when to use it, why it's helpful, and how to make it your own. It commits the result to [`outputs/`](./outputs/) and sends Jeremy a short Telegram ping pointing at the dashboard, it does not dump the draft into chat.

It never posts to Skool itself. Jeremy reads and copies the draft from the dashboard, edits if needed, ships it.

## How it's wired

This runs on the ClaudeClaw bot's own scheduler, not a hosted Claude Code Routine, so there's no separate web UI to maintain. See `docs/solutions/` in the claudeclaw repo (`orphaned-cron-prompt-scheduled-tasks-2026-07-02.md`) for why recurring work in that project always goes through the local scheduler. To change the schedule or the wrapper prompt, edit task `bb0fece4` via the `schedule` skill; to change what the routine actually does, edit `ROUTINE.md` in this repo, the scheduler prompt just points at it.

## How to read the output

- **Dashboard (primary):** Mission Control → Skills Weekly (`/skills-weekly`, shortcut `g k`) reads every file in `outputs/` on Jeremy's Mac and renders them as a scrollable feed, newest first, each with a one-click copy button. Backend route: `src/dashboard/routes/skills-weekly.ts` in the claudeclaw repo.
- `outputs/caios-skill-<slug>-YYYY-MM-DD.md`, that week's post, ready to paste into Skool
- Each file is append-only (the routine never modifies past runs)
- Git history = your archive of every post you've shipped

## How to tune

- Add/reorder skills to cover → edit [`inputs/skills-queue.md`](./inputs/skills-queue.md)
- Change voice, audience, or genericization rules → edit [`.claude/CLAUDE.md`](./.claude/CLAUDE.md)
- Change the post format itself → edit the OUTPUT section of [`ROUTINE.md`](./ROUTINE.md)

## Kill date

Review after the queue in `inputs/skills-queue.md` runs out (currently 15 weeks of material): kill, restock the queue, or promote to a real backend.
