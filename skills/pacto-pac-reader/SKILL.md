---
name: pacto-pac-reader
description: Look up and read Pacto PACs from the covenant-gov/.github docs/PAC directory.
allowed-tools:
  - Read
  - Bash
  - Ask
---

# pacto-pac-reader

## Triggers

- "Look up PAC-1"
- "Read PAC-1"
- "What does PAC-1 say?"
- "Find the PAC about proposal types"
- "PAC lookup"
- "Show me the PACs"
- "List PACs"

## What to do

1. Extract the PAC number or keywords from the user's request.
2. Find the matching file(s) in `covenant-gov/.github/docs/PAC/`:
   - Prefer the local path `~/src/covenant-gov/.github/docs/PAC/` if it exists.
   - Otherwise, list `https://api.github.com/repos/covenant-gov/.github/contents/docs/PAC` with `gh api` or `curl` and parse the JSON.
3. If the user gave an exact number (e.g., PAC-1), match the filename pattern `PAC-{N}-*.md`.
4. If the user gave keywords, search PAC filenames and titles.
5. Read the matching file:
   - Local: `read(~/src/covenant-gov/.github/docs/PAC/{filename})`
   - Remote: `https://raw.githubusercontent.com/covenant-gov/.github/main/docs/PAC/{filename}`
6. Return the content. If it is long, offer to summarize or quote specific sections.
7. If the user asks for a list, return the available PAC numbers and titles.

## Rules

- If no PAC matches, say so and list available PACs.
- If multiple PACs match, ask the user to clarify.
- Do not hallucinate PAC content; always read the actual file.
- When quoting, reference the PAC number and section.
- Prefer local files when available; fall back to GitHub raw URLs.
