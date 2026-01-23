# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Working Relationship

- Push back on ideas when warranted - cite sources and explain reasoning
- ALWAYS ask for clarification rather than making assumptions
- NEVER lie, guess, or make up information

## Project Overview

This is a Mintlify documentation site using MDX (Markdown + JSX) for content authoring.

- Format: MDX files with YAML frontmatter
- Config: `docs.json` for navigation, theme, settings
- Components: Mintlify custom components

## Development Commands

```bash
# Install CLI (one-time setup, requires Node.js 19+)
npm i -g mint

# Start local dev server (runs at http://localhost:3000)
mint dev

# Run on custom port
mint dev --port 3333

# Update CLI to latest version
npm mint update

# Validate links in documentation
mint broken-links
```

## Project Structure

- `docs.json` - Main configuration file controlling navigation, theming, logos, and site settings
- `*.mdx` files - Documentation pages written in MDX format
- `snippets/` - Reusable content snippets that can be imported into other pages
- `api-reference/openapi.json` - OpenAPI spec for auto-generated API documentation
- `images/` and `logo/` - Static assets

## Content Strategy

- Document just enough for user success - not too much, not too little
- Prioritize accuracy and usability of information
- Make content evergreen when possible
- Search for existing information before adding new content - avoid duplication unless strategic
- Check existing patterns for consistency
- Start by making the smallest reasonable changes

## Frontmatter Requirements

Every MDX page requires:
- `title`: Clear, descriptive page title
- `description`: Concise summary for SEO/navigation

## Writing Standards

- Second-person voice ("you")
- Prerequisites at start of procedural content
- Test all code examples before publishing
- Match style and formatting of existing pages
- Include both basic and advanced use cases
- Language tags on all code blocks
- Alt text on all images
- Relative paths for internal links

## Available Components

`<Card>`, `<CardGroup>`, `<Accordion>`, `<AccordionGroup>`, `<Steps>`, `<Step>`, `<Tip>`, `<Note>`, `<Warning>`, `<Info>`, `<Frame>`, `<Columns>`, `<ResponseField>`, `<Expandable>`, `<CodeGroup>`

## Git Workflow

- NEVER use `--no-verify` when committing
- Ask how to handle uncommitted changes before starting
- Create a new branch when no clear branch exists for changes
- Commit frequently throughout development
- NEVER skip or disable pre-commit hooks

## Do Not

- Skip frontmatter on any MDX file
- Use absolute URLs for internal links
- Include untested code examples
- Make assumptions - always ask for clarification

## Deployment

Changes pushed to the default branch are automatically deployed via the Mintlify GitHub app.
