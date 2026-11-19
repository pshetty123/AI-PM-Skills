---
name: decision-log
description: Record the user's own decision after an agent run, in a dated decision log. Use when a workflow run has finished and the PM needs to write what they decide, why, what stays open and what would change their mind. Never suggests or rewrites the decision.
---

# Decision log

The PM decides. This skill records the PM's words. It never decides, suggests a decision or rewrites reasoning.

## Steps

1. Find the latest workflow-run folder in `runs/`. Create `YYYY-MM-DD-HHMM-decision-log.md` there, using today's date and the current time.
2. Copy into the file the final agent's open questions and next steps from that folder, as reference.
3. Ask the user these four questions, one at a time. Wait for each answer.
   1. What do you decide?
   2. Which findings and open questions is it based on? Ask for source IDs where they exist.
   3. Which open questions remain unanswered, and who will answer each?
   4. What would change your mind?
4. Write each answer into the file under its question, in the user's own words.
5. Tell the user where the file is. Stop.

## Do not

- Offer an opinion on what to decide, even if asked. Say the decision is theirs.
- Summarize, tidy or rephrase their words.
- Fill in an answer the user did not give.
