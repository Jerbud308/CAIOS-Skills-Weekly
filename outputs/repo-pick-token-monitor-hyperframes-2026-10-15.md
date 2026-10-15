# Repo picks: Watch your plan limits, make client videos from a prompt

> **Not yet approved.** Picked by repo-radar on usage signals, not personally vetted. Check its box in the vault list if you're good with it.

Ranking evidence: Javis603/token-monitor score 87.7 (usage 31.9, usability 25), 69.3 stars/day, 35 outside issue authors in 30 days. heygen-com/hyperframes score 88.5 (usage 29.6, usability 25), 818.8 stars/day, 19 outside issue authors in 30 days.

## My Agent OS

You're deep into a job and your agent just stops, because you hit your plan limit and had no idea you were close.

Token Monitor is a small desktop widget that shows how much you've used and where your plan limits sit. It works across Claude Code, Codex, Cursor and a few other tools, so you see it all in one place instead of guessing. Your prompts and code stay on your machine. It's MIT licensed.

The catch: it's a desktop app, so it lives on the computer you install it on. Syncing across several devices is optional and takes extra setup, and for some providers the limit checks need a cookie or an API key.

Try this: on a Mac, run brew install --cask token-monitor, or grab the download from the GitHub Releases page. Leave it running for a day and see which tool eats your budget.

https://github.com/Javis603/token-monitor

## AI Transformation Hub

Lane: serving clients. A client asks for a short product video, and you don't have an editor or a week to spare.

HyperFrames turns plain HTML into an MP4. You describe the video to Claude Code, something like "a 10-second product intro with a fade-in title, a background video and subtle music", and it builds it as a page and renders it out. It installs as a Claude Code plugin, and it's Apache-2.0.

The catch: it's built for agents, not for clicking around. You need Claude Code and Node 22 or newer. If that sounds like too much, hand it to whoever on your team already works in the terminal.

Try this: run claude plugin marketplace add heygen-com/hyperframes, then claude plugin install hyperframes@hyperframes, and make one intro clip for your own business before you offer it to a client.

https://github.com/heygen-com/hyperframes

---
*Repo picks, a RAC Projects AI production.*
