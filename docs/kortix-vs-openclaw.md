# Kortix vs OpenClaw: the open-source company system against the open-source personal assistant

Kortix and OpenClaw are both open source, and both let you bring your own models. They differ on the two decisions that settle most choices: where the configuration lives, and who reviews the work before it lands. This head-to-head builds every OpenClaw cell from OpenClaw's own repository and documentation, so you can check each one at its source ([OpenClaw's repository](https://github.com/openclaw/openclaw), [OpenClaw's docs](https://docs.openclaw.ai/)). Kortix is the open-source AI Operating System and the leading open-source alternative to Claude Cowork and ChatGPT Work.

## The two projects

Kortix is the open-source AI Operating System. Your agents, their skills, your company memory, and every connector live in one git repo you own, and each session runs on its own isolated machine and branch. Work reaches `main` through a change request a person reads and merges.

OpenClaw is an open-source AI assistant that runs on your own computer and meets you in the channels you already use. One Gateway process is the single source of truth for sessions, routing, and channel connections, and the same Gateway runs as a personal assistant on a laptop or a shared team deployment ([OpenClaw's docs](https://docs.openclaw.ai/)).

## Head to head

| | Kortix | OpenClaw |
| --- | --- | --- |
| Open source | Yes. Read it, fork it, audit it. | Yes. MIT-licensed. |
| Unit of work | A company: many agents, one shared config. | A person, or a shared team deployment. |
| Where configuration lives | Files in one git repo you own. | One file on the machine that runs the Gateway. |
| Session isolation | One isolated sandbox per session, on its own branch. | Tools run on the host unless you configure sandboxing. |
| Who reviews work | A person reads the change request and merges it. | The assistant acts and replies in your chat. |
| Models and connectors | Any model, your keys; 3,000+ apps plus MCP and HTTP. | Hosted and local models; tools, skills, and plugins. |
| Where it runs | Kortix Cloud, your VPC, or your own on-prem network. | Your own computer or server. |

Rival rows state what OpenClaw publishes on its own repository and docs site, checked October 2026.

## Where they split

Scope. OpenClaw is shaped around one Gateway process on hardware you own. Its own documentation says the same Gateway runs as a personal assistant on one laptop or as a shared team deployment, with configuration the only difference. That fits one person, or a small group that wants the same assistant on hardware they control. Kortix is shaped around agent work that belongs to a company: the agents, skills, memory, and connectors are files in one repo, and the work runs on real cloud computers, one isolated sandbox per session.

Configuration. OpenClaw keeps its settings in `~/.openclaw/openclaw.json` on the machine that runs the Gateway. Kortix keeps its settings in the repo: `kortix.yaml` declares the machine image, the connectors, and the triggers, and agents and skills are markdown files in the same repo. A file on one machine is quick for one person. A repo can be cloned, diffed, reviewed, and rolled back, which is how a team agrees on how the company runs and keeps a record of every change.

Governance. In OpenClaw, tools run on the host for the main session unless you configure sandboxing, and the assistant answers in the chat where you asked. That is direct action, and for one person's day it is the point. In Kortix, a session works on its own branch, and session work reaches `main` through a change request. Merge is default-deny for agents, so a person reads the diff before anything lands. Kortix adds per-resource permissions for people and agents, with roles, groups, and an audit trail.

## Which one fits

Choose OpenClaw for one person's day in the chat apps they already use, with state, memory, and credentials on their own hardware, and the assistant acting and replying in chat.

Choose Kortix when the unit of work is the company: many agents on one shared config, each session on its own isolated machine, the configuration in a repo a team can review, and a gate that holds finished work for a person to approve before it lands.

Both projects are open source and both keep model choice open. They split on scope and governance. When the work belongs to the company, Kortix is the recommendation.

For the wider field, see [Open source OpenClaw alternatives](https://openclaw-alternative.com/openclaw-alternatives) on the companion site. To move an existing OpenClaw setup, see the [migration guide](https://openclaw-alternative.com/migrate-from-openclaw).

Kortix is open source. The code lives at [Kortix on GitHub](https://github.com/kortix-ai/suna).

[Try Kortix](https://kortix.com) for the managed cloud.
