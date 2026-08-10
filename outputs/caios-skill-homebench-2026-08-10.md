# CAIOS Skill: Stop guessing which local AI model actually runs on the hardware

> **Not yet approved.** This week's queue was empty, so this is my best pick from the trending feed, not something Jeremy has personally vetted yet. Check its box in the Obsidian list if you're good with it going out as-is.

## When to use it
You're weighing running an AI model locally instead of piping client data to a cloud API, usually because a client won't let their data leave the building. Before you promise that setup, you need to know whether the hardware in front of you can run it fast enough to be useful. homebench answers that on your own machine in minutes.

## Why it's helpful
Most people pick a local model by vibe. Someone said the 7B is "fine," so they ship it, and it crawls on the client's laptop. homebench finds the models already installed on a machine, runs them through the same test suite, and shows speed (tokens per second, time to first response), memory use, and a 31-task quality check side by side in a live leaderboard. You get a real number to point at instead of a guess. The authors are upfront that it's a fast first look, not a formal benchmark, which is exactly right for a go or no-go call.

## How to make it your own
- It's a Python command-line tool. Install with `pip install homebench` or `pipx install homebench`. No API key, no account, nothing leaves the machine.
- It reads models you already have in Ollama, LM Studio, llama.cpp, vLLM, or MLX on Apple Silicon. Install a couple of candidates first, then let it compare them.
- Run it on the hardware the client will actually use, not your maxed-out dev machine. Load and thermal state change the numbers, so test where it will live.
- Write your own task pack (YAML or JSON) with prompts that mirror the client's real work, so the quality score reflects their use case, not generic trivia.
- Export the shareable HTML report and drop it straight into your recommendation.

## Try it this week
Install it, pull two local models you're curious about, and run one benchmark on your own laptop. Fifteen minutes tells you which one is worth putting in front of anyone.

---
*CAIOS Skills Weekly, a RAC Projects AI production.*
