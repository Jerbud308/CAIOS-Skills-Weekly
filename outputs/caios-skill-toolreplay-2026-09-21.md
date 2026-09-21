# CAIOS Skill: Read the Receipt Before You Trust the Agent

> **Not yet approved.** This week's queue was empty, so this is my best pick from the trending feed, not something Jeremy has personally vetted yet. Check its box in the Obsidian list if you're good with it going out as-is.

## When to use it
You've put an agent into a client's workflow and someone asks what you can't answer from memory: did it only do what we said it could, and why did it cost that much? ToolReplay reads a log of the agent's tool calls and reports where it repeated work it already did, where the same call returned two different answers, and where it used a tool it was never granted.

## Why it's helpful
The usual review is scrolling a transcript and trusting your eyes. That catches the obvious failure and misses the expensive one. Repeated calls are the quiet money leak, and the rule here is conservative on purpose: it only flags a repeat when nothing in between could have changed the answer. The scope check maps to what a client's IT lead will ask. Hand it a one-line file listing the tools that agent may call, and it names every call that stepped outside. It also hash-chains a session, which proves a sealed log is unedited, not that whoever sealed it was honest.

## How to make it your own
- Python 3.11 or newer, no other dependencies, no network calls. It never runs your real tools, only reads what was recorded.
- The catch: it reads its own strict format, one JSON line per call with exactly four fields. Nothing emits that natively, so someone has to convert your agent's logs first. That conversion is the real adoption cost.
- Write a scope file per agent role. Worth doing even if you never run the tool, because almost nobody has written down what their agent may touch.
- It exits non-zero on a finding, so it drops into an automated check without extra wiring.
- MIT licensed, so you can build it into something you sell.

## Try it this week
Run its two audit commands against the dirty sample in the repo. Six calls, one of each problem, and you'll see what an audit of your own agent looks like.

---
*CAIOS Skills Weekly, a RAC Projects AI production.*
