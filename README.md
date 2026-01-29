# Portfolio Assignment - Claude Skills Framework

This repository contains a Claude Code skills framework that extends Claude's capabilities through custom functionality modules called "skills". These skills can be invoked automatically by Claude when relevant or directly using slash commands.

## What This Project Does

This project implements a skill-based extension system for Claude Code that provides specialized functionality in several areas:

- **Daily Work Summarization**: Converts unstructured daily work data into clean, structured summaries
- **Document Polishing**: Transforms messy notes into clean, structured internal documents
- **Meeting Insights Extraction**: Extracts key information from meeting transcripts into structured summaries
- **Financial Market Updates**: Provides cryptocurrency and forex market updates and insights
- **General Productivity**: Additional tools to enhance Claude's capabilities

## Skills Included

### Daily Work Summarizer
- **Name**: `daily-work-summarizer`
- **Purpose**: Converts unstructured daily work data into structured summaries with completed work, blockers, decisions, and next actions

### Internal Document Polisher
- **Name**: `internal-doc-polisher`
- **Purpose**: Converts messy notes into clean, structured internal documents with consistent tone and proper formatting

### Meeting Transcript Insight Extractor
- **Name**: `meeting-transcript-insight-extractor`
- **Purpose**: Extracts key information from meeting transcripts into structured summaries with decisions, action items, and deadlines

### Crypto Market Updates
- **Name**: `crypto-market-updates`
- **Purpose**: Fetches and summarizes the latest cryptocurrency market updates, price movements, and blockchain events

### Forex News Fetcher
- **Name**: `forex-news-fetcher`
- **Purpose**: Fetches and summarizes the latest forex market updates, currency movements, and economic events

## How to Use

### Prerequisites
- Claude Code installed and configured
- Access to Anthropic API (if using Claude)

### Installation
1. Clone this repository to your local machine
2. Place the `.claude` directory in your project root or in your home directory for global access
3. The skills will be automatically available in Claude Code

### Usage
Skills can be invoked in two ways:
1. Automatically by Claude when it detects relevant context
2. Directly using slash commands like `/skill-name` (e.g., `/daily-work-summarizer`)

For skills that accept arguments, pass them after the command:
```
/daily-work-summarizer [your daily notes here]
```

## Project Structure

```
├── .claude/
│   └── skills/
│       ├── daily-work-summarizer-skill/
│       ├── internal-doc-polisher-skill/
│       ├── meeting-transcript-insight-extractor-skill/
│       ├── crypto-market-updates-skill/
│       └── forex-news-fetcher-skill/
└── CLAUDE.md
```

Each skill is contained in its own directory with a `SKILL.md` file that defines:
- YAML frontmatter with configuration
- Markdown content with instructions for Claude
- Input/output specifications
- Usage guidelines

## Creating New Skills

To create a new skill:

1. Create a new directory in `.claude/skills/` with the name followed by `-skill`
2. Create a `SKILL.md` file with the following structure:

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
Description of what kind of input the skill expects.

## Output
Description of what the skill produces.

## Instructions

Step-by-step instructions for Claude when the skill is invoked:
1. Take the input provided by the user
2. Process it according to the requirements
3. Generate the appropriate output format
4. Follow any specific formatting guidelines
```

## Security Considerations

- The `.mcp.json` file (if present) contains sensitive credentials and is excluded from version control via `.gitignore`
- Never commit API keys, tokens, or other sensitive information to the repository
- Review all skills for potential security implications before deployment

## License

This project is designed as an educational assignment for extending Claude Code capabilities through custom skills.