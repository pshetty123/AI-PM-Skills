---
name: run-checker
description: Check an agent run before passing its output to the next agent. Verifies the "Files read" line, that no agent read files outside its context, that every cited source ID exists, and that points carry labels. Use after each agent run in a multi-agent workflow.
---

# Run checker

Check one agent output before it moves on. Stop the run on any failure and tell the user. Never pass a failed output forward.

## Checks

1. **Files read line.** The output begins with a "Files read:" line that lists file paths. If missing, fail.
2. **Context boundary.** Every listed file is inside that agent's allowed Context, as written in its agent file. If it read anything else, fail and name the file.
3. **Citations exist.** Every source ID cited (for example SRC-01) appears in `context/sources.md`. If an ID does not exist, fail and name it.
4. **Citations present.** Every claim carries at least one source ID. List claims without one.
5. **Labels.** If the agent's Output requires labels such as known, assumed or unknown, every point has one.
6. **Role.** The output stays in the agent's role. For example, a research agent gives no recommendations and a challenger gives no plan.

## Report

Show a short table: check, pass or fail, detail. End with one line: "Safe to pass on" or "Stop: fix first". Do not fix the output yourself unless the user asks.
