# Agent hub

This repository is a hub of personal agents. Each agent is a folder under
`agents/` containing an `AGENT.md` that fully specifies its job. Schedules
live in Claude Code scheduled tasks, which simply say "run agent X".

## Running an agent

When asked to run an agent (by a person or a scheduled task):

1. Read `agents/<name>/AGENT.md` and follow it exactly.
2. Read `agents/PROFILE.md` for who the owner is and what they care about;
   every agent tailors its output to that profile.
3. Deliver the output the way the agent's "Delivery" section says.

## Adding an agent

1. Copy `agents/_template/` to `agents/<new-name>/` and fill in `AGENT.md`.
2. Add a row to the registry table in `agents/README.md`.
3. If it should run on a schedule, create a scheduled task whose prompt is
   "Run the `<new-name>` agent from the agent hub", plus a copy of the
   agent's instructions as fallback (see the existing task for the pattern).

Keep shared facts about the owner in `agents/PROFILE.md`, not in individual
agents, so every agent benefits from an update.
