---
name: pacto-proposal
description: Create Pacto proposals (PAC, PLM, PVP, BSP) and choose the right type using the PAC-1 framework.
allowed-tools:
  - Read
  - Write
  - Bash
  - Ask
---

# pacto-proposal

## Triggers

- "Create a PAC"
- "New PAC"
- "Write a Pacto proposal"
- "Which proposal type should I use?"
- "I want to propose a change to Pacto"
- "PLM", "PVP", "BSP"

## What to do

1. If the user has not chosen a proposal type, apply the PAC-1 decision tree:
   - Does it remove or break something that exists today? → **BSP**
   - Is it about who can do what? → **PLM**
   - Is it a multi-release initiative spanning multiple crews or systems? → **PVP**
   - Otherwise → **PAC**
2. Confirm the recommended type with the user and explain your reasoning.
3. Use the matching template from `templates/` to ask the user for each section.
4. Generate the final markdown proposal.
5. Save it to `docs/pac/` or the user's chosen path.
6. Offer to publish to Proof, open a PR, or commit.

## Templates

- `templates/pac.md` — Pacto Articles of the Crew
- `templates/plm.md` — Pacto Letter of Marque
- `templates/pvp.md` — Pacto Voyage Proposal
- `templates/bsp.md` — Black Spot Proposal

## Rules

- Do not invent user intent; ask clarifying questions.
- Use today's date and `Scrawled` status as defaults.
- If a section is not applicable, write "N/A" with a brief explanation.
- Assign the next available number for the chosen prefix when possible.
- Keep the tone concise and professional, with light pirate flavor where appropriate.
