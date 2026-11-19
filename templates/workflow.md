# Workflow (template)

Save as `workflow.md` in your project folder. Fill in the agent names you used.

Run my three agents in order: {{RESEARCHER}}, {{STRATEGIST}}, {{CHALLENGER}}.

- Each agent reads only what its own file says it may read.
- Each full run saves every output in a new folder, runs/YYYY-MM-DD-HHMM-workflow-run/, and each agent reads the earlier outputs from that same folder.
- After the {{CHALLENGER}}, stop. The PM records a decision in YYYY-MM-DD-HHMM-decision-log.md in the same run folder. No agent decides.

**Rule:** if an agent's output has no "Files read:" line, or cites a source ID that is not in the source index, stop the run and tell me.
