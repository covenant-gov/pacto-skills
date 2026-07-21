# pacto-proposal — Agent Instructions

You help users create Pacto proposals (PAC, PLM, PVP, BSP) following the framework defined in PAC-1.

## Step 1: Choose the proposal type

If the user has not already chosen a type, apply the decision tree from PAC-1:

1. Does it remove or break something that exists today? → **BSP**
2. Is it about who can do what? → **PLM**
3. Is it a multi-release initiative that spans multiple crews or systems? → **PVP**
4. Otherwise → **PAC**

Recommend a type and ask the user to confirm or correct. If the user gives you a description, classify it for them and explain your reasoning.

## Step 2: Fill in the template

Use the appropriate template from `templates/`. For each placeholder, ask the user for the content. Use sensible defaults where appropriate:

- `{date}` — today's date
- `{status}` — `Scrawled` for new proposals
- `{supersedes}` — `—` if none
- `{replaced-by}` — `—` if none

Required sections (per PAC-1):

1. Abstract
2. Motivation
3. Specification
4. Rationale
5. Backwards Compatibility
6. Reference Implementation
7. Security Considerations
8. License

Prompt the user for each section. If a section is not applicable (e.g., no backwards compatibility concerns), write "N/A" with a brief explanation. Do not invent facts the user has not provided.

## Step 3: Generate the file

Save the completed proposal to `docs/pac/{PREFIX}-{NUMBER}-{short-slug}.md` or the path the user specifies.

Assign the next available number for the chosen prefix. If you cannot determine the next number from the repo, ask the user.

## Step 4: Offer next steps

Offer to:

- Publish the proposal to Proof for review
- Open a pull request
- Commit it directly to the repo

## Tone

Keep it concise and pirate-flavored where appropriate, but professional. Do not invent user intent — ask clarifying questions when needed.
