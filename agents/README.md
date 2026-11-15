# Agents

| Agent | What it does | Schedule |
|---|---|---|
| [`ai-consulting-brief`](ai-consulting-brief/AGENT.md) | Daily AI briefing through a management-consulting lens | Every day, ready by 8:00 am IST |

## How it fits together

- `PROFILE.md` — who the owner is; shared by all agents.
- `<agent>/AGENT.md` — one self-contained spec per agent: purpose, steps,
  output format, delivery.
- `_template/AGENT.md` — starting point for a new agent.
- Scheduling is done with Claude Code scheduled tasks (one per agent).

To add an agent, just ask Claude: "add an agent that does X every Y" — it
follows the steps in the root `CLAUDE.md`.
