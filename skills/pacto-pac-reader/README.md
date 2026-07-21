# pacto-pac-reader

Look up and read Pacto PACs from the `covenant-gov/.github` repository.

## Triggers

- "Look up PAC-1"
- "Read PAC-1"
- "What does PAC-1 say?"
- "Find the PAC about proposal types"
- "PAC lookup"
- "Show me the PACs"
- "List PACs"

## What it does

1. Parses the user's request for a PAC number or keywords.
2. Finds the matching file in `docs/PAC/`.
3. Reads the full markdown content.
4. Returns the content or a summary of the requested section.

## Source

PACs are stored at:
https://github.com/covenant-gov/.github/tree/main/docs/PAC

The skill prefers the local clone at `~/src/covenant-gov/.github/docs/PAC/` and falls back to GitHub raw URLs.

## Examples

- "What does PAC-1 say about proposal types?"
- "List all PACs"
- "Read the PAC about scope and threshold"
