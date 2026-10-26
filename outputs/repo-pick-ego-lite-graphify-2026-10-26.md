# Repo picks: let your agent browse without taking over your tabs, and map a client folder before day one

> **Not yet approved.** Picked by repo-radar on usage signals, not personally vetted. Check its box in the vault list if you're good with it.

Ranking evidence: citrolabs/ego-lite score 88.4 (usage 24.6, usability 25), 281.3 stars/day, 33 outside issue authors in 30 days. Graphify-Labs/graphify score 90.5 (usage 31.4, usability 25), 995.0 stars/day, 27 outside issue authors in 30 days.

## My Agent OS

Ever asked your agent to do something in a browser and watched it take over your tabs? This one fixes that.

ego-lite is a free browser built for AI agents. Each agent works in its own separate Space inside the same browser, so you keep browsing in yours and the agent never grabs your tabs. It works with Claude Code, Codex and Cursor through a skill called ego-browser, and your data stays on your device.

The catch: it's a separate browser app you install, Mac and Windows for now. On first launch it asks if you want to bring over your Chrome data, which carries your logins. If you say yes, the agent can use those logged-in sessions, so go slow with that part.

Try this: install it with npx skills add citrolabs/ego-lite, then tell your agent: /ego-browser follow @ego_agent on x.com for me.

https://github.com/citrolabs/ego-lite

## AI Transformation Hub

Serving clients: before an engagement you usually get handed a folder of docs, some code and a pile of PDFs, and you have to work out how it all connects.

Graphify is a skill for Claude Code, Cursor, Codex and Gemini CLI that turns code, docs, PDFs, images and video into a knowledge graph you can ask questions of. Code is read locally with nothing leaving the machine. Docs, PDFs and images go through your assistant's model or an API key you set up. Each link in the graph is tagged as found in the source or inferred, so you can see what's a guess.

The catch: it's a command line install that needs Python 3.10 or newer. That makes it a tool for whoever on your team handles technical setup, not something to hand a client. There's also an optional paid cloud version.

Try this: uv tool install graphifyy, then graphify install, then run /graphify . on a folder of sample material.

https://github.com/Graphify-Labs/graphify

---
*Repo picks, a RAC Projects AI production.*
