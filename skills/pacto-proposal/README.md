# pacto-proposal

Create Pacto proposals: PAC, PLM, PVP, and BSP.

## Trigger phrases

- "Create a PAC"
- "New PAC"
- "Write a Pacto proposal"
- "Which proposal type should I use?"
- "I want to propose a change to Pacto"
- "PLM", "PVP", "BSP"

## What it does

1. Helps you choose the right proposal type (PAC, PLM, PVP, BSP) using the decision tree from PAC-1.
2. Asks you questions to fill in the proposal template.
3. Generates a correctly formatted markdown file.
4. Saves the file to `docs/pac/` or your chosen location.

## Proposal types

- **PAC** — Pacto Articles of the Crew: new features, standards, rules, protocols
- **PLM** — Pacto Letter of Marque: permissions, capabilities, authorizations
- **PVP** — Pacto Voyage Proposal: multi-stage initiatives, roadmaps
- **BSP** — Black Spot Proposal: deprecation, removal, or breaking changes

See [PAC-1](https://github.com/covenant-gov/.github/blob/main/docs/PAC/PAC-1-the-articles-of-the-crew.md) for the full framework.

## Decision tree

```
Does it remove or break something that exists today? → BSP
Is it about who can do what? → PLM
Is it a multi-release initiative spanning multiple crews or systems? → PVP
Otherwise → PAC
```
