# CAIOS Skill: Your AI agent read the rules. Did it follow them?

> **Not yet approved.** This week's queue was empty, so this is my best pick from the trending feed, not something I've personally vetted yet. Check its box in the Obsidian list if you're good with it going out as-is.

## When to use it

Any time you're letting an AI coding agent make real edits to something you or a client depends on, especially a long session where you're not watching every single change.

## Why it's helpful

Most people write their AI agent a rulebook once (keep it simple, don't add dependencies, don't overbuild) and then just hope. There's nothing actually checking whether the agent followed any of it. This tool watches every edit as it happens and reports back into the same session: a new dependency that snuck into the manifest, a wrapper function that just forwards to another function and does nothing else, a single-use abstraction that didn't need to exist. You see it while the agent is still working, not three days later in review when it's already tangled into everything else.

It's a coding tool specifically, it needs Node and git installed, and it's built for people actually running an AI coding agent. If that's not you day to day, the tool itself isn't for you. The habit underneath it is, and that's the part worth stealing either way.

## How to make it your own

- Pick your enforcement level to match how much you trust the session: flag-only for early exploration, block-on-certain-violations once you're shipping something real.
- If you don't write code yourself, ask whoever runs your AI agents (a dev, a vendor, an internal team) whether they have anything watching for this. Most don't.
- Steal the checklist even without the tool: at the end of any AI-delegated task, ask specifically "what new dependencies, files, or abstractions did you introduce, and did each one earn its place?" That's the exact question this tool automates.
- The pattern generalizes past code: don't just tell an AI (or a person) your rules once. Put a mechanical check on whether they were actually followed.

## Try it this week

Next time you hand an AI agent a real task, don't just review the final result. Ask it to list everything new it added, and make it justify each one before you accept the work.

---
*CAIOS Skills Weekly, a RAC Projects AI production.*
