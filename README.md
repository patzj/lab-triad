# Lab Triad

A small workspace for learning agentic web security assessment using Codex or OpenCode, with Hack The Box Web Challenges, PortSwigger Web Security Academy, and vulnerable web apps like DVWA.

Uses up to three agents:

- **Orchestrator:** Your main session. Plans the assessment, runs tests, and explains the results.
- **Analyst:** Examines source code or traffic and proposes exploit hypotheses.
- **Challenger:** Questions assumptions and checks whether the evidence supports the findings.

## Getting started

Follow [SETUP.md](SETUP.md) to configure your chosen harness and optional integrations.

1. Open a terminal in the project root.
2. Start your chosen harness:

   ```sh
   codex
   ```

   Or:

   ```sh
   opencode
   ```

3. Open the appropriate prompt:
   - `prompts/blackbox.md` for testing without server source code.
   - `prompts/whitebox.md` for testing with source code.
4. Fill in the target URL, objective, available accounts, and source path if applicable.
5. Paste the completed prompt into your main session.

The main session acts as the orchestrator and delegates to the specialists when useful. Only the orchestrator sends requests or controls your proxy.

## Files

| File or directory     | Purpose                                                |
| --------------------- | ------------------------------------------------------ |
| `README.md`           | Project overview and usage.                            |
| `SETUP.md`            | Requirements and integration setup.                    |
| `AGENTS.md`           | Shared assessment rules for both harnesses.            |
| `.codex/config.toml`  | Codex configuration, including the two-subagent limit. |
| `.codex/agents/`      | Codex analyst and challenger definitions.              |
| `.opencode/agents/`   | OpenCode analyst and challenger definitions.           |
| `prompts/blackbox.md` | Starts an assessment without server source code.       |
| `prompts/whitebox.md` | Starts an assessment with source code.                 |

## Learning from an assessment

Ask the agents to explain:

- Why they chose a test and what result they expected.
- How the observed behavior supports or disproves a hypothesis.
- Why an exploit worked and which assumptions it violated.
- What failed attempts actually ruled out.

The agents should verify the lab objective before claiming success. They should not search for walkthroughs unless you request it.

Test only your assigned lab instance and its supporting services. Keep source code unchanged so the results reflect the original application.
