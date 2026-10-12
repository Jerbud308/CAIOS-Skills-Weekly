# Repo picks: Keep the agent from forgetting, govern what your clients' teams run

> **Not yet approved.** Picked by repo-radar on usage signals, not personally vetted. Check its box in the vault list if you're good with it.

Ranking evidence: mksglu/context-mode score 89.6 (usage 30.3, usability 25), 353.7 stars/day, 34 outside issue authors in 30 days. Observal/Observal score 79.3 (usage 28.0, usability 25), 40.7 stars/day, 8 outside issue authors in 30 days.

## My Agent OS

You know the moment your agent is deep into a big job, the chat compacts, and suddenly it forgets what it already did? A plugin called context-mode is built for exactly that.

Instead of stuffing every huge tool result into the conversation, it keeps the raw output out of the way. It also logs your edits, tasks and errors in a small database, so after a compact the agent can look things up instead of guessing.

The catch: setup is a few steps, not one click. You add it from the plugin marketplace, install it, restart, then run a doctor command to confirm it worked. It needs Claude Code v1.0.33 or newer, and the license is Elastic License 2.0, which is source-available rather than standard open source.

Try this: run /plugin marketplace add mksglu/context-mode, follow the install steps in the README, restart, and run the doctor check.

https://github.com/mksglu/context-mode

## AI Transformation Hub

Lane: serving clients. A client's team starts using AI coding agents, and a month later nobody can say which skills, MCP servers or prompts are in use, who approved them, or what changed.

Observal is a self-hosted registry built for that. Agent resources live in one place, an admin reviews and approves submissions, version diffs show what changed, and session traces let you replay what an agent did for an audit. It also generates configs for Claude Code, Codex, Cursor and Copilot, and reports on what people actually use.

The catch: this is not something to hand a client's ops person. The server needs Docker Engine 24 or newer with Compose v2, and a command line tool goes on each developer's machine. Whoever on your team handles infrastructure should run it. It's Apache-2.0.

Try this: stand it up on your own machine and register a couple of your own skills, so you can show a client what governance looks like before you scope it.

https://github.com/Observal/Observal

---
*Repo picks, a RAC Projects AI production.*
