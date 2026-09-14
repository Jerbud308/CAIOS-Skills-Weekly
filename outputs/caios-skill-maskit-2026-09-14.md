# CAIOS Skill: Keep Client Data Off the Model Without Wrecking the Workflow

> **Not yet approved.** This week's queue was empty, so this is my best pick from the trending feed, not something Jeremy has personally vetted yet. Check its box in the Obsidian list if you're good with it going out as-is.

## When to use it
The client says their data can't go to an outside AI provider. Or you're about to paste a config file, a connection string, or a customer list into an AI coding tool and you know you shouldn't. Maskit sits between your tool and the model, swapping sensitive values for placeholders on the way out and restoring them in the answer as it streams back.

## Why it's helpful
The usual fix is asking people to redact by hand, which fails the first busy Tuesday. This runs in the request path, so it happens whether anyone remembers or not. Placeholders stay consistent across a conversation, so a name maps to the same token on turn 1 and turn 20 and the model's reasoning holds up. Everything runs locally.

The honest limit: it only works where you can set your own API base URL. It does nothing for someone pasting a client document into a browser chat window, which is how most people actually leak things.

## How to make it your own
- Desktop app (Windows or Apple Silicon Mac), then point one tool's base URL at the local port. Docker for a team. You bring your own API key.
- Turn on the rules you need. Only 7 of the 19 built-ins are on by default, and the credential-heavy ones ship off: PEM private keys, cloud access keys, JWTs, bearer tokens.
- Three of those defaults (mobile, landline, national ID) match Chinese formats. Clients elsewhere means writing your own patterns.
- Load a wordlist of client names, project codenames, and staff names. Generic rules never catch those, and those are what identify an engagement.
- AGPL-3.0, so check the license before building it into anything you sell. The project is also days old. Promising, not proven.

## Try it this week
Point one tool at it, send a prompt with a fake connection string, then read the request log to see what actually left your machine.

---
*CAIOS Skills Weekly, a RAC Projects AI production.*
