---
name: internal-doc-polisher
description: Converts messy notes into clean, structured internal documents with consistent tone, proper formatting, and logical flow. Use when you need to transform unstructured notes into professional internal docs, README files, or proposals.
argument-hint: [document-type] [raw-notes]
---

# Internal Doc Polisher

Converts messy notes into clean, structured internal documents with consistent tone, proper formatting, and logical flow.

## What this skill does

Transforms unstructured input into professional internal documents:
- Internal documentation
- README files
- Proposals
- Technical specifications
- Meeting summaries

Enforces:
- Consistent tone and style
- Clear structure and formatting
- Logical flow of information
- Professional language

## Input
Unstructured notes such as:
- Bullet points and lists
- Fragmented sentences
- Brain dumps
- Chat or meeting notes
- Rough ideas and concepts

## Output
A well-structured internal document with:
- Clear sections and headers
- Logical flow of information
- Consistent professional tone
- Readable, polished language

## Document Templates

Choose the most appropriate format based on context:

### General Internal Document
- Title
- Background/Context
- Current Issues (if applicable)
- Proposed Solutions (if applicable)
- Implementation Steps (if applicable)
- Timeline (if applicable)
- Conclusion

### README
- Title and description
- Installation/setup instructions
- Usage examples
- Configuration details
- Contributing guidelines
- License information

### Proposal
- Title
- Problem Statement
- Proposed Solution
- Benefits
- Implementation Plan
- Timeline
- Resources Required

## Instructions

Process $ARGUMENTS by:
1. Identifying the main topics or themes in the raw notes
2. Organizing content into logical sections
3. Expanding fragmented thoughts into complete sentences
4. Applying the most appropriate document template
5. Ensuring consistent professional tone throughout
6. Checking for clarity and readability

If $ARGUMENTS includes a specific document type (e.g., "readme", "proposal"), use the corresponding template. Otherwise, use the general internal document format.