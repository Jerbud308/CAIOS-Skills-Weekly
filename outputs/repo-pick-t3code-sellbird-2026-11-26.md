# Repo picks: approve your agent from your phone, and cold outreach that waits for your OK

> **Not yet approved.** Picked by repo-radar on usage signals, not personally vetted. Check its box in the vault list if you're good with it.

Ranking evidence: pingdotgg/t3code score 99.8 (usage 34.8, usability 25.0), 2059.0/day, 38 outside issue authors in 30 days. ethanplusai/sellbird score 90.5 (usage 29.0, usability 25.0), 112.9/day, 15 outside issue authors in 30 days.

## My Agent OS

You start a long task in Claude Code, walk away from your desk, and it sits there waiting on one yes or no.

T3 Code is a free, open source app that runs the coding agents already on your computer, Claude Code included, and gives them one interface. It has iOS and Android apps, so you can approve the next step from your phone. It drives the agents you're already signed in to, so it doesn't resell tokens or add a bill.

The catch: it's built for people who write code, so expect some setup. You install the desktop app, sign in to an agent, then follow its remote access doc to connect your phone over your local network, Tailscale, or T3 Connect. The phone part is the fiddly bit.

Try this: on a Mac, run brew install --cask t3-code, sign in to Claude Code, and run one thread in it before you touch the phone side.

https://github.com/pingdotgg/t3code

## AI Transformation Hub

Your own outreach is the first thing that slips when client delivery gets busy. This one is for the getting clients lane.

Sellbird is an open source outreach tool that runs on your own machine. It finds businesses that match your customer, reads their websites for buying signals, finds the owner, checks the email address, writes a personal cold email and handles the replies. By default nothing sends until you approve it. It thinks through Claude Code on your Claude plan, so there's no model API bill.

The catch: it's cold email, so you need a mailbox to send from (ideally a separate domain), warmup on it, and an address checker. Setup means Python 3.11 or newer and a terminal, so it's one for whoever on your team is comfortable there. The license is AGPL-3.0.

Try this: skip the sending. Find and verify a list for one niche, run sellbird export, and judge the quality yourself.

https://github.com/ethanplusai/sellbird

---
*Repo picks, a RAC Projects AI production.*
