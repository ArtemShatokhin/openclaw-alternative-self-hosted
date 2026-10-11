# What is OpenClaw? A primer from OpenClaw's own materials, and the open-source Kortix alternative

OpenClaw is a self-hosted gateway that connects the chat apps you already use to an AI assistant running on your own machine. You run a single Gateway process on your machine or a server, and it becomes the bridge between your messaging apps and an always-available assistant ([OpenClaw's docs](https://docs.openclaw.ai/)). This primer takes each fact from OpenClaw's own repository and documentation, then shows where the design stops for company work and where Kortix, the open-source AI Operating System, takes over.

## What OpenClaw does

OpenClaw meets you in the channels you already use. Its documentation lists Discord, Google Chat, iMessage, Matrix, Microsoft Teams, Signal, Slack, Telegram, WhatsApp, and Zalo, with more added through channel plugins, and one Gateway serves every configured channel at the same time ([OpenClaw's docs](https://docs.openclaw.ai/)). Native apps cover macOS, iOS, Android, Windows, and Linux, so the same assistant follows you from phone to desktop ([OpenClaw's repository](https://github.com/openclaw/openclaw)).

One Gateway serves either a personal assistant on a laptop or a shared team deployment, and OpenClaw's documentation calls configuration the only difference between the two. State, memory, and credentials live on the hardware you run it on, and models and agent harnesses such as Claude, Codex, or a local model are plugins you can swap.

OpenClaw documents its own license as MIT, and it is stewarded by the OpenClaw Foundation, an independent 501(c)(3) with no paid tier, hosted service, or token ([OpenClaw's repository](https://github.com/openclaw/openclaw)). Installation runs through a shell installer on macOS, Linux, and Windows, or the published package on Node 24.16+ or 26.1+, as documented in October 2026.

## What OpenClaw is not

OpenClaw is an assistant, and its own materials say so. A shared team deployment is still one assistant with more people talking to it. Tools run on the host for the main session unless you configure sandboxing, inbound messages are treated as untrusted input, and the documented architecture is a trusted gateway with untrusted execution ([OpenClaw's repository](https://github.com/openclaw/openclaw)). Configuration lives in one file, `~/.openclaw/openclaw.json`, on the machine that runs the Gateway.

The gap appears when the work belongs to a company. Configuration sits on one machine instead of in a shared repository. No single file states what each agent may touch. No gate holds finished work for a person to approve before it takes effect.

## OpenClaw at a glance

Each row is what OpenClaw states about itself on its own repository or documentation.

| Dimension | What OpenClaw documents |
| --- | --- |
| What it is | A self-hosted gateway that connects chat apps to an AI assistant. |
| Where it runs | Your own machine or server; state and credentials stay local. |
| Channels | Discord, iMessage, Slack, Teams, Telegram, WhatsApp, and more via plugins. |
| Configuration | One file, `~/.openclaw/openclaw.json`, on the host. |
| Models | Hosted and local providers; harnesses are swappable plugins. |
| License | Open source, MIT-licensed, stewarded by the OpenClaw Foundation. |
| Governance | Tools run on the host unless you configure sandboxing. |

## What Kortix is

Kortix is the open-source AI Operating System: your agents, their skills, your company memory, and every connector in one git repo you own, with the agents working on real cloud computers. Each session has its own isolated machine and branch, thousands of agents run in parallel on one config, and session work reaches `main` through a change request a person reads and merges.

The difference from OpenClaw is where the configuration lives and who reviews the work. Kortix keeps the agents, skills, memory, and connectors as files in a repo the whole company can clone, diff, and roll back, and it holds finished work for review before it lands.

For the full definition and where the two projects differ, see [What is OpenClaw](https://openclaw-alternative.com/what-is-openclaw) on the companion site, and the [head-to-head](kortix-vs-openclaw.md) in this repository.

Kortix is open source. The code lives at [Kortix on GitHub](https://github.com/kortix-ai/suna).

[Try Kortix](https://kortix.com) for the managed cloud.
