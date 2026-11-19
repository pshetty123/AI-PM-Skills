# AI PM Team Skills

Four small skills for Claude Code that go with the workshop **Multi-Agent Architecture: Your AI PM Team, For Product Managers**, by Priyanka Shetty (The AI Pitstop).

The idea: agents do the analysis, the PM keeps the call.

| Skill | What it does |
|---|---|
| `agent-builder` | Interviews you for the five fields (Role, Context, Instructions, Guardrails, Output) and writes the agent file from your answers. |
| `decision-log` | Records your own decision, the findings it rests on, open questions and what would change your mind. It never decides for you. |
| `break-test` | Tries to break an agent's guardrails: out-of-role requests, a deleted source, conflicting data, a hidden instruction. |
| `run-checker` | Checks an agent output before it moves on: Files read line, context boundary, cited IDs that exist, labels, role. |

## Templates

Reusable versions of the agents from the workshop, with the case-specific details replaced by fill-in fields. Open a template, fill the `{{FIELDS}}` listed at the top, and save it in your `agents/` folder.

| Template | What it is |
|---|---|
| `templates/agent-template.md` | The five fields, with one rule under each. |
| `templates/researcher.md` | Finds what is true. Facts only, every claim cited, split into Known, Assumptions and Unknowns. |
| `templates/strategist.md` | Turns findings into options. Never reads the raw evidence. |
| `templates/challenger.md` | Reads everything. Asks questions and suggests checks. Never plans. |
| `templates/workflow.md` | The run order, the run folder and the stop rule. |

## Install

1. Click **Code**, then **Download ZIP**, and unzip it.
2. Copy the folders inside `skills/` into your Claude Code skills folder:
   - for one project: `.claude/skills/` inside your project folder
   - for every project: `~/.claude/skills/`
3. Start Claude Code and ask for a skill by name, for example: "Use the agent-builder skill to build an agent for my launch go or no-go decision."

## Status

Version 0.1. Written for the workshop. Run each skill once on your own case and adjust the wording to your needs.

## License

MIT. See `LICENSE`.
