---
name: daily-work-summarizer
description: Converts unstructured daily work data into a clean, structured summary with completed work, blockers, decisions, and next actions. Use when you need to transform raw work notes into a professional daily or weekly summary.
argument-hint: [daily-notes]
---

# Daily Work Summarizer

Transforms unstructured daily work data into a clean, structured summary.

## What this skill does

Takes raw daily notes and produces a structured summary with:

- ✅ What was done
- ⚠️ Blockers
- 🧠 Decisions made
- ⏭️ Next actions
- Clear outcome

## Input
Unstructured daily work data, such as:
- Bullet notes you wrote during the day
- Slack/Teams messages
- Git commit messages
- Meeting notes

## Output
A structured daily or weekly summary with:
- ✅ Work completed
- ⚠️ Blockers
- 🧠 Decisions made
- ⏭️ Next actions

## Template for Output

Daily Work Summary – [Date]

Completed:
- [List completed tasks]

In Progress:
- [List tasks still in progress]

Blockers:
- [List items blocking progress]

Decisions:
- [List important decisions made]

Next Actions:
- [List next planned actions]

## Instructions

When processing $ARGUMENTS, organize the information according to the template above. Identify completed tasks, ongoing work, blockers, decisions made, and next steps. Group similar items together and rephrase for clarity and professionalism.