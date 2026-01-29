---
name: meeting-transcript-insight-extractor
description: Extracts key information from meeting transcripts or notes into a structured summary with decisions, action items, owners, and deadlines. Use when you need to convert meeting notes into a clear action list.
argument-hint: [meeting-transcript]
---

# Meeting Transcript Insight Extractor

Extracts key information from meeting transcripts or notes into a structured summary.

## What this skill does

Takes meeting transcripts or notes and extracts:
- Decisions made during the meeting
- Action items assigned
- Owners responsible for each action
- Deadlines for completion
- Open questions or unresolved topics

## Input
- Meeting transcript (full text of meeting)
- Rough meeting notes (bullet points, fragments)

## Output
A structured meeting summary containing:
- ✅ Decisions made
- 🧑‍💼 Action items with owners
- ⏰ Deadlines (if mentioned)
- ❓ Open questions or unresolved items

## Template for Output

Meeting Summary – [Topic]

Decisions:
- [List decisions made during the meeting]

Action Items:
- [Owner]: [Action to be taken] (by [deadline] if mentioned)

Open Questions:
- [List unresolved topics or items needing follow-up]

## Instructions

When processing $ARGUMENTS, carefully read through the meeting content and identify:

1. Explicit decisions that were made (look for phrases like "we decided", "agreed to", "will proceed with")
2. Action items assigned to specific individuals (look for phrases like "[name] will", "[name] can handle", "assigned to [name]")
3. Deadlines mentioned for action items (dates, timeframes, or relative timeframes like "tomorrow", "by Friday")
4. Open questions or unresolved topics that need follow-up

Format the extracted information according to the template above, keeping descriptions concise but clear. Group action items by owner when possible.