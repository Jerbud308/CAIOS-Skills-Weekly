# CAIOS Skills Weekly

A RAC Projects AI production. A Claude Code Routine that publishes one "steal this" AI skill breakdown a week, written for the AITP Skool community: consultants and AI transformation partners, not developers.

## What this does

Every Monday at 08:00 AM, Claude Code runs [`ROUTINE.md`](./ROUTINE.md). It picks the next skill from the queue, reads the real SKILL.md behind it, and writes a Skool-ready post: what it is, when to use it, why it's helpful, and how to make it your own. It commits the result to [`outputs/`](./outputs/).

It never posts to Skool itself. You paste the draft in, edit if needed, ship it.

## Setup

1. Fork or clone this repo.
2. Connect it as the destination repo when you create the routine at [claude.ai/code/routines](https://claude.ai/code/routines).
3. Paste the contents of [`ROUTINE.md`](./ROUTINE.md) as the prompt.
4. Trigger: weekly cron at `0 8 * * 1` (Monday 8am).
5. Save. First run happens at the next Monday 08:00.

## How to read the output

- `outputs/caios-skill-<slug>-YYYY-MM-DD.md`, that week's post, ready to paste into Skool
- Each file is append-only (the routine never modifies past runs)
- Git history = your archive of every post you've shipped

## How to tune

- Add/reorder skills to cover → edit [`inputs/skills-queue.md`](./inputs/skills-queue.md)
- Change voice, audience, or genericization rules → edit [`.claude/CLAUDE.md`](./.claude/CLAUDE.md)
- Change the post format itself → edit the OUTPUT section of [`ROUTINE.md`](./ROUTINE.md)

## Kill date

Review after the queue in `inputs/skills-queue.md` runs out (currently 15 weeks of material): kill, restock the queue, or promote to a real backend.
