# Repo picks: mark up the plan, brief the call

> **Not yet approved.** Picked by repo-radar on usage signals, not personally vetted. Check its box in the vault list if you're good with it.

Ranking evidence: backnotprop/plannotator score 92.5 (usage 31.5, usability 25), 329.4/day, 27 outside issue authors in 30 days. mvanhorn/last30days-skill score 92.2 (usage 29.8, usability 25), 782.8/day, 21 outside issue authors in 30 days.

## My Agent OS

When Claude Code hands you a plan, you either skim it in the terminal and say yes, or you scroll back up trying to remember what you wanted to change. Plannotator fixes that part.

When the agent proposes a plan or finishes a task, it opens in your browser. You mark it up, comment on specific lines, and send the feedback straight back to the agent. It does the same for diffs and pull requests. It runs locally and it's Apache-2.0.

The catch: the installer sets up hooks, skills and slash commands in your agent config, and it's a curl-pipe-to-bash script. Read it first, or add the --minimal flag to install only the binary.

Try this: ask Claude Code for a plan on something small, then mark up one line of it instead of retyping your reply.

https://github.com/backnotprop/plannotator

## AI Transformation Hub

Before a discovery call, most of us do the same thing: open a pile of tabs, skim the website, find a LinkedIn post. last30days is a Claude skill that does a faster version of that.

You give it a topic or a company. It searches Reddit, Hacker News, Polymarket and GitHub, scores what it finds by real engagement, and writes you a brief. For a company it also checks patent filings and careers pages, which shows what they're building before they announce it. That's the getting-clients lane: walking into the call knowing something specific.

The catch: those four sources need zero setup. X, TikTok and YouTube need a setup wizard and often API keys, and some of those sources are paid.

Try this: run it on your next prospect's company name and read the brief before you open their site.

https://github.com/mvanhorn/last30days-skill

---
*Repo picks, a RAC Projects AI production.*
