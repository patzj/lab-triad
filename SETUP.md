# Setup

This workspace is for web application assessments using HTB Web
Challenges, PortSwigger Web Security Academy, and vulnerable web apps
such as DVWA.

## Requirements

- An authenticated Codex CLI or OpenCode installation.
- Access to an assigned web lab instance.
- For OpenCode, credentials for your selected model provider.

## Agent configuration

Agent definitions are included for both harnesses:

- Codex: `.codex/agents/`
- OpenCode: `.opencode/agents/`

Both use the project-root `AGENTS.md` and the prompts in `prompts/`.

Start your chosen harness from the project root.
Use one orchestrator at a time.

## Optional: Caido

Install the official `caido-mode` skill with project scope for your
chosen harness. Complete its dependency setup and authentication:

https://docs.caido.io/app/tutorials/skills

If already installed and working, skip this step.

## Optional: Burp Suite MCP (untested)

Burp Suite MCP has not been tested with this workspace.

If configured, verify the connection and available tools before use.
Choose one primary proxy for each assessment.

## Lab files

Store challenge source in `labs/`, captured evidence in `artifacts/`,
and working notes in `notes/`. These directories are ignored by Git.

Keep credentials and authentication caches out of Git.

See README.md for starting a black-box or white-box web assessment.
