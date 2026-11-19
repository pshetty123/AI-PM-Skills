# Agent template: the five fields

Copy this file to `agents/<agent-name>.md` and fill in each field. One rule sits under each heading.

## Role
Who the agent is, with one job described in one sentence.

## Context
The exact files the agent may read, including its own definition file. Nothing else. Also list what it must NOT read.

## Instructions
The steps the agent follows, in order.

## Guardrails
What the agent must never do, written so that someone can test it.

## Output
The exact format the agent returns, with named sections and numbering. Start with a "Files read:" line. This format is the next agent's input.
