# CLAUDE Guidelines

To talk and give answers in a professional and academic tone.

## About Skills

Skills extend Claude's capabilities by allowing custom functionality through SKILL.md files. These can be invoked automatically by Claude when relevant or directly using slash commands like `/skill-name`.

### Creating Skills

Skills are defined in `SKILL.md` files with two main components:
1. YAML frontmatter (between `---` markers) that tells Claude when to use the skill
2. Markdown content with instructions Claude follows when the skill is invoked

When creating skills, name the skill directory with the name of the skill followed by "-skill" at the end (e.g., "notes-generator-skill", "code-analyzer-skill", "api-tester-skill").

Example structure:
```yaml
---
name: skill-name
description: What the skill does and when to use it
---

Instructions for Claude when the skill is invoked...
```

### Skill Storage Locations

Skills can be stored at different levels:
- Personal: `~/.claude/skills/<skill-name>/SKILL.md` (available across all projects)
- Project: `.claude/skills/<skill-name>/SKILL.md` (project only)
- Enterprise: Managed settings (organization-wide)

### Frontmatter Configuration

Key fields for configuring skills:
- `name`: Display name (lowercase, numbers, hyphens only)
- `description`: What the skill does (recommended)
- `disable-model-invocation`: Prevent Claude from auto-invoking (true/false)
- `user-invocable`: Hide from user menu (true/false)
- `allowed-tools`: Tools Claude can use with this skill
- `context`: Set to `fork` to run in subagent

### Argument Handling

Skills can accept arguments:
- `$ARGUMENTS`: All arguments passed to the skill
- `$ARGUMENTS[0]`, `$ARGUMENTS[1]`: Specific arguments by index
- `$0`, `$1`: Short form for specific arguments

### Advanced Features

Skills support advanced functionality:
- Dynamic context injection using `!command` syntax
- Running in subagents with `context: fork`
- Supporting files in the skill directory
- String substitutions for dynamic values

## Proper Skill Structure

When creating a new skill, use the following structure as a template:

```yaml
---
name: skill-name
description: What the skill does and when to use it
disable-model-invocation: false
user-invocable: true
allowed-tools:
  - Bash
  - Read
  - Edit
  - Write
  - Grep
  - Glob
context: fork
---

# Skill Title

Brief description of what this skill does.

## What this skill does

Detailed explanation of the skill's functionality and purpose.

## Input
Description of what kind of input the skill expects, such as:
- Text data to process
- Files to analyze
- Parameters to use

## Output
Description of what the skill produces:
- Processed data
- Formatted results
- Generated content

## Instructions

Step-by-step instructions for Claude when the skill is invoked:
1. Take the input provided by the user
2. Process it according to the requirements
3. Generate the appropriate output format
4. Follow any specific formatting guidelines

Additional notes about how the skill should operate.
```

## Behavior When Using Skills

When asking about topics related to any skill, Claude should return the requested information directly rather than the skill's structure or output format. For example:
- When asking for crypto market updates, Claude should provide the actual market information, not explain the crypto-market-updates skill
- When asking for forex news, Claude should provide the actual forex market updates, not explain the forex-news-fetcher skill
- When asking for meeting insights, Claude should extract the relevant information, not explain the meeting-transcript-insight-extractor skill

## Existing Skills

The following skills are already available in this project:

### Daily Work Summarizer
- **Name:** daily-work-summarizer
- **Description:** Converts unstructured daily work data into a clean, structured summary with completed work, blockers, decisions, and next actions
- **Purpose:** Transform raw work notes into professional daily or weekly summaries
- **Input:** Unstructured daily work data (bullet notes, chat messages, etc.)
- **Output:** Structured summary with completed tasks, blockers, decisions, and next actions

### Forex News Fetcher
- **Name:** forex-news-fetcher
- **Description:** Fetches and summarizes the latest forex market updates, currency movements, and relevant economic events
- **Purpose:** Provide current information about foreign exchange markets, currency pairs, and economic events affecting forex trading
- **Input:** Optional currency pair and date range parameters
- **Output:** Structured summary of forex market updates and insights

### Crypto Market Updates
- **Name:** crypto-market-updates
- **Description:** Fetches and summarizes the latest cryptocurrency market updates, price movements, and relevant blockchain events
- **Purpose:** Provide current information about digital assets, cryptocurrency prices, and market trends
- **Input:** Optional cryptocurrency symbol and timeframe parameters
- **Output:** Structured summary of cryptocurrency market updates and insights

### Internal Doc Polisher
- **Name:** internal-doc-polisher
- **Description:** Converts messy notes into clean, structured internal documents with consistent tone, proper formatting, and logical flow
- **Purpose:** Transform unstructured notes into professional internal docs, README files, or proposals
- **Input:** Unstructured notes, bullet points, brain dumps, or rough ideas
- **Output:** Well-structured internal documents with appropriate templates

### Meeting Transcript Insight Extractor
- **Name:** meeting-transcript-insight-extractor
- **Description:** Extracts key information from meeting transcripts or notes into a structured summary with decisions, action items, owners, and deadlines
- **Purpose:** Convert meeting notes into a clear action list
- **Input:** Meeting transcripts or rough meeting notes
- **Output:** Structured summary with decisions, action items, owners, and deadlines
