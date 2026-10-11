# OpenClaw alternative FAQ: the open-source Kortix AI Operating System

Short answers to the questions teams ask before they move company work from OpenClaw to Kortix, the open-source AI Operating System.

## Is Kortix open source?

Yes. Kortix is the open-source AI Operating System, and the code is public: read it, fork it, audit it. The source lives at [Kortix on GitHub](https://github.com/kortix-ai/suna). Self-host is free, and you connect your own model keys.

## How is Kortix different from OpenClaw for a company?

OpenClaw runs as one Gateway on your own computer, and its tools run on the host unless you configure sandboxing ([OpenClaw's repository](https://github.com/openclaw/openclaw)). Kortix holds your agents, skills, memory, and connectors in one git repo you own. Each session has its own isolated machine and branch, and session work reaches `main` through a change request a person reads and merges.

## Can several agents run at the same time?

Yes. Thousands of agents in parallel on one config, each on its own cloud computer, with no crossover between sessions. Kortix reaches 3,000+ apps in a click, plus MCP, OpenAPI, Postman, GraphQL, and raw HTTP, and connector credentials are brokered server-side and never enter the machine.

## What does Kortix give a security team?

One isolated sandbox per session. Per-resource permissions for people and agents, with roles, groups, and an audit trail. SAML 2.0 single sign-on and SCIM 2.0. Secrets are encrypted at rest with a key per project. Run it on Kortix Cloud, in your VPC, or on your own on-prem network. SOC 2 Type I is held, and SOC 2 Type II is in progress.

## Can I keep OpenClaw too?

Yes. Many teams keep OpenClaw for a personal assistant on one machine and run Kortix for company agent work. The two keep separate state, so each uses its own keys and channels. The companion site walks the file-by-file move in its [migration guide](https://openclaw-alternative.com/migrate-from-openclaw).

## What does it cost?

Self-host is free, and you pay only your own model and compute bills. The managed cloud is the paid option, and the plans are published at [Kortix pricing](https://kortix.com/pricing).
