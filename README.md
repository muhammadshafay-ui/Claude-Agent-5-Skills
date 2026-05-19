# Portfolio Assignment - Claude Skills Framework

This repository contains a Claude Code skills framework that extends Claude's capabilities through custom functionality modules called "skills". These skills can be invoked automatically by Claude when relevant or directly using slash commands.

## Project Demo
      
Watch a short walkthrough of the Claude Agent 5 Skills project in action. The video showcases the main features, the user interface, and a quick demo of the
agent’s capabilities.
      
[![Demo video]]([https://github.com/muhammadshafay-ui/Claude-Agent-5-Skills/raw/main/assets/project-demo.mp4](https://github.com/muhammadshafay-ui/Claude-Agent-5-Skills/blob/master/assets/Portfolio%20Assignment.mp4))
      
*Click the thumbnail above to play the video directly from the repository.*

## What This Project Does

This project implements a skill-based extension system for Claude Code that provides specialized functionality in several areas:

- **Daily Work Summarization**: Converts unstructured daily work data into clean, structured summaries
- **Document Polishing**: Transforms messy notes into clean, structured internal documents
- **Meeting Insights Extraction**: Extracts key information from meeting transcripts into structured summaries
- **Financial Market Updates**: Provides cryptocurrency and forex market updates and insights
- **General Productivity**: Additional tools to enhance Claude's capabilities

## Benefits of Using These Skills

### Time Savings
- **Daily Work Summarizer**: Saves 15-30 minutes daily vs manual report creation
- **Internal Document Polisher**: Saves 20-40 minutes per document vs manual formatting
- **Meeting Transcript Extractor**: Saves 10-25 minutes per meeting vs manual review
- **Market Update Skills**: Save 15-30 minutes daily vs checking multiple sources manually

### Quality Improvements
- **Consistency**: All outputs follow standardized templates and professional formatting
- **Completeness**: Skills systematically extract all relevant information vs human reviewers who might miss items
- **Professionalism**: Automated language refinement ensures consistent professional tone
- **Accuracy**: Systematic processing reduces human error in data extraction and formatting

### Process Automation
- **Eliminates Repetitive Tasks**: No more manually copying notes into structured formats
- **Reduces Context Switching**: Get information directly in your workflow without visiting multiple sites
- **Standardizes Outputs**: All documents follow consistent structure regardless of original input format
- **Improves Accountability**: Clear assignment of action items and deadlines from meetings

## Manual Processes Replaced

### Daily Work Summarization
- **Previously**: Manually compiling scattered notes, chat messages, and task lists into structured reports
- **Now**: One command transforms all inputs into a professional daily/weekly summary

### Document Creation
- **Previously**: Formatting documents from scratch, ensuring consistent styling, and refining rough notes
- **Now**: Paste rough notes and get professionally formatted documents instantly

### Meeting Follow-ups
- **Previously**: Listening to recordings, manually extracting action items, assigning owners, tracking deadlines
- **Now**: Automatic extraction of decisions, action items, owners, and deadlines from transcripts

### Market Monitoring
- **Previously**: Checking multiple financial/crypto news sites, aggregating data, analyzing trends separately
- **Now**: Consolidated updates on demand with relevant analysis and context

## Skills Included

### Daily Work Summarizer
- **Name**: `daily-work-summarizer`
- **Purpose**: Converts unstructured daily work data into structured summaries with completed work, blockers, decisions, and next actions
- **Replaces**: Manual compilation of daily/weekly reports, copying notes into structured formats
- **Time Saved**: 15-30 minutes per day vs manual report creation
- **Quality Improved**: Consistent format, professional language, comprehensive coverage of all work aspects

### Internal Document Polisher
- **Name**: `internal-doc-polisher`
- **Purpose**: Converts messy notes into clean, structured internal documents with consistent tone and proper formatting
- **Replaces**: Manual editing of rough notes, formatting documents from scratch, applying consistent styles
- **Time Saved**: 20-40 minutes per document vs manual formatting and editing
- **Quality Improved**: Professional formatting, consistent tone, logical structure, polished language

### Meeting Transcript Insight Extractor
- **Name**: `meeting-transcript-insight-extractor`
- **Purpose**: Extracts key information from meeting transcripts into structured summaries with decisions, action items, and deadlines
- **Replaces**: Manually reviewing meeting recordings/transcripts, extracting action items, assigning owners
- **Time Saved**: 10-25 minutes per meeting vs manual review and extraction
- **Quality Improved**: Complete capture of decisions and action items, clear ownership assignments, organized follow-ups

### Crypto Market Updates
- **Name**: `crypto-market-updates`
- **Purpose**: Fetches and summarizes the latest cryptocurrency market updates, price movements, and blockchain events
- **Replaces**: Visiting multiple crypto news sites, aggregating market data, analyzing price movements manually
- **Time Saved**: 15-30 minutes daily vs checking multiple sources
- **Quality Improved**: Comprehensive coverage of major coins, timely updates, consolidated information from multiple sources

### Forex News Fetcher
- **Name**: `forex-news-fetcher`
- **Purpose**: Fetches and summarizes the latest forex market updates, currency movements, and economic events
- **Replaces**: Checking multiple financial news sites, monitoring currency pairs manually, aggregating economic events
- **Time Saved**: 15-30 minutes daily vs manual market monitoring
- **Quality Improved**: Real-time updates, comprehensive coverage of major pairs, economic context integration

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
