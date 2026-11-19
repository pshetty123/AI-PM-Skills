---
name: agent-builder
description: Build one AI agent definition file by interviewing the user for the five fields (Role, Context, Instructions, Guardrails, Output), one at a time. Use when the user wants to create or redesign an agent for a recurring decision.
---

# Agent builder

Create one agent file from the user's own answers. The user decides what goes in each field. Never invent an answer.

## Steps

1. Check for `agents/template.md`. If it exists, use its five headings. If not, use: Role, Context, Instructions, Guardrails, Output.
2. Ask for each field one at a time, in this order. Wait for the answer before asking the next.
   - **Role:** What is the one job this agent does, in one sentence? Push back if it lists several jobs.
   - **Context:** Which exact files may it read, including its own definition file? Nothing else. Ask which files it must NOT read.
   - **Instructions:** What steps does it follow, in order?
   - **Guardrails:** What must it never do? Each rule must be testable by someone else. Push back on vague rules such as "be careful".
   - **Output:** What is the exact format it returns, with named sections and numbering? Start the output with a "Files read:" line. This format is the next agent's input.
3. If any answer is missing, vague or contradicts an earlier one, ask a follow-up before moving on.
4. Show the full draft file and ask the user to confirm or change it.
5. After confirmation, create `agents/<agent-name>.md`. Use the user's words. Do not add rules the user did not give.

## Do not

- Write the fields for the user.
- Add strategy, recommendations or extra guardrails on your own.
- Create the file before the user confirms the draft.
