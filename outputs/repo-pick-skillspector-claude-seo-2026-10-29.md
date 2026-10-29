# Repo picks: check a skill before you install it, and audit a prospect site on the first call

> **Not yet approved.** Picked by repo-radar on usage signals, not personally vetted. Check its box in the vault list if you're good with it.

Ranking evidence: NVIDIA/SkillSpector score 93.5 (usage 29.5, usability 25), 335.1 stars/day, 20 outside issue authors in 30 days. AgriciDaniel/claude-seo score 89.3 (usage 29.3, usability 25), 658.3 stars/day, 19 outside issue authors in 30 days.

## My Agent OS

Before you add a skill someone shared online to your agent, it's worth knowing what's inside it. A skill is instructions your agent follows, so a bad one can quietly do things you never asked for.

SkillSpector is a free scanner from NVIDIA that checks a skill before you install it. Point it at a folder, a zip, a GitHub link or a single SKILL.md. It checks for 71 known risky patterns and gives you a risk score from 0 to 100 plus a readable report.

The catch: it runs in a terminal and needs Python 3.12 or newer. The deeper check uses an AI model, so it wants an API key. The quick check does not, just add the --no-llm flag.

Try this: take the next skill you were about to install, run skillspector scan ./that-skill/ --no-llm, and read what it flags before you say yes.

Install: uv tool install git+https://github.com/NVIDIA/skillspector.git

https://github.com/NVIDIA/skillspector

## AI Transformation Hub

Lane: getting clients. You are on a first call with a business owner and you'd like to show them something real before you send a proposal.

Claude SEO is a free Claude Code plugin that audits a website. Type /seo audit and the site's address. Specialist agents run in parallel, about 10 to 15 minutes by the README, and you get a prioritized action plan as Markdown, PDF or JSON. It covers technical SEO, content quality, schema, and how visible the site is in AI search like ChatGPT and Google AI Overviews.

The catch: this is for you, not something you hand to the client. It runs inside Claude Code on your machine, so you or a teammate comfortable in the Code tab runs it, and you walk the client through the report. Setup builds its own Python environment and a headless browser. No API keys needed, though connecting free Google ones adds real field data.

Try this: audit your own site this week and see what you'd flag. Install is three commands.

https://github.com/AgriciDaniel/claude-seo

---
*Repo picks, a RAC Projects AI production.*
