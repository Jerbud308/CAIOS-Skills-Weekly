# Repo picks: Watch the meter, read the prospect

> **Not yet approved.** Picked by repo-radar on usage signals, not personally vetted. Check its box in the vault list if you're good with it.

Ranking evidence: vinzdg/codenotch score 82.4 (usage 33.3, usability 25), 84.2 stars/day over its lifetime, 29 outside issue authors in 30 days. every-app/open-seo score 64.1 (usage 30.1, usability 25), stars/day pending (one snapshot so far), 26 outside issue authors in 30 days.

## My Agent OS

Your agent stops mid-task because you hit your Claude limit. Or you walk away, come back an hour later, and it's been sitting there waiting on you.

Codenotch puts a small black notch on the edge of your screen. Each ring shows how much of a usage limit you've burned, and hovering shows when it resets. Claude's ring uses the same session window as Claude Code's own /usage, so the two never disagree. It also shows whether a session is still working, done, or stuck waiting on you. Codex, Cursor and plenty of other tools get rings too.

The catch: it reads your numbers off the Claude login already on your machine. Claude Desktop's usage cache first, then Claude Code's /usage or the sign-in token in your keychain. You're trusting a brand-new app with that. The Mac download is signed and updates itself. There's a Windows version, but its installer isn't code-signed.

Try this: install it, switch off every provider except Claude, and leave it running for one normal workday.

https://github.com/vinzdg/codenotch

## AI Transformation Hub

This one's for the getting-clients lane. Before a call with a prospect, you want to know where they rank, who's beating them, and what's broken on their site. Semrush and Ahrefs do that, but the subscription is a lot for a handful of prospect pulls a month.

OpenSEO is an open source alternative. It covers keyword research, rank tracking, competitor insights, backlinks, site audits and AI visibility. It also runs an MCP server with pre-built skills, so Claude Code can pull the data and work with it for you.

The catch: no subscription, but you need a DataForSEO API key and you pay them for every request. Self-hosting means Docker on your own machine, or Cloudflare if your team shares it, so hand setup to whoever on the team is comfortable with that. The hosted version skips setup but charges 28% on top of each data request.

Try this: pick one prospect you're talking to this month, run a site audit and a competitor check, and bring the three biggest findings to the call.

https://github.com/every-app/open-seo

---
*Repo picks, a RAC Projects AI production.*
