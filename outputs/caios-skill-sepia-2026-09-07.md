# CAIOS Skill: The tell isn't the word choice, it's the structure

> **Not yet approved.** This week's queue was empty, so this is my best pick from the trending feed, not something Jeremy has personally vetted yet. Check its box in the Obsidian list if you're good with it going out as-is.

## When to use it

An agent drafted your client update, and it reads like a machine wrote it. You cut "delve", swapped a few sentences, and it still does. sepia treats that giveaway as a structural problem, not a vocabulary one.

## Why it's helpful

Most humanizers only edit the surface: word choice, syntax, clichés. The research behind sepia found that for fiction, a classifier reading narrative structure alone still catches AI writing after editors fix the surface. So it works in three passes: architecture, then flow, then surface. Business prose fails differently, and the repo says so plainly, with its own rules: filler carrying no information, hedging where a judgment was needed, register that ignores the venue. The principle worth stealing outright: calibrate toward how humans actually write, don't invert every AI habit, because applying every rule at once just creates a new fingerprint. It picks three to five moves per piece and leaves slack.

## How to make it your own

- It installs into a coding-agent CLI, not a browser chat. One command, `npx skills add Nanako0129/sepia -g`, covers Claude Code, Codex, Cursor and others. If a chat tab is your whole setup, steal the three-layer method by hand.
- Start in diagnose-only mode. It reports what's wrong without touching the text, which is how you learn your own tells instead of outsourcing them.
- Know what ships. Half the repo targets fiction, and the business documents it covers are release notes, replies, postmortems, tickets and technical articles. Client proposals aren't one, so you'll lean on the shared checklist and the generic review and rewrite modes.
- Tell it which model wrote the draft. It carries per-model tells and applies them only when it knows.
- Brand-voice layering is labeled experimental, backed by "a worked example, not measured evidence." Treat it that way.

## Try it this week

Take the last agent-assisted thing you sent a client, run the review pass, and read the diagnosis without changing a word.

---
*CAIOS Skills Weekly, a RAC Projects AI production.*
