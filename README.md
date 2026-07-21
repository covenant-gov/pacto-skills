# pacto-skills

Agent skills for the [Pacto](https://github.com/covenant-gov/pacto-app) ecosystem.

This repository contains skills that help humans and AI agents work with Pacto's pirate-themed improvement framework: **PACs** (Pacto Articles of the Crew), **PLMs** (Letters of Marque), **PVPs** (Voyages), and **BSPs** (Black Spots).

The canonical framework is defined in [PAC-1](https://github.com/covenant-gov/.github/blob/main/docs/PAC/PAC-1-the-articles-of-the-crew.md) in the [`covenant-gov/.github`](https://github.com/covenant-gov/.github) repository.

## Available skills

| Skill | Purpose | Location |
|-------|---------|----------|
| `pacto-proposal` | Create Pacto proposals (PAC, PLM, PVP, BSP) and choose the right type | [`skills/pacto-proposal`](./skills/pacto-proposal) |
| `pacto-pac-reader` | Look up and read Pacto PACs from the `.github` repository | [`skills/pacto-pac-reader`](./skills/pacto-pac-reader) |

## Install

These skills are installed using the [Vercel skills CLI](https://github.com/vercel-labs/skills):

```bash
# Install all pacto-skills
npx skills add covenant-gov/pacto-skills

# Install a specific skill
npx skills add covenant-gov/pacto-skills --skill pacto-proposal
npx skills add covenant-gov/pacto-skills --skill pacto-pac-reader

# List available skills in this repo
npx skills add covenant-gov/pacto-skills --list
```

## Usage

### `pacto-proposal`

Trigger phrases:

- "Create a PAC"
- "Write a Pacto proposal"
- "Which proposal type should I use?"
- "I want to propose a change to Pacto"

The skill will guide you through choosing the right type and filling in the template.

### `pacto-pac-reader`

Trigger phrases:

- "Look up PAC-1"
- "What does PAC-1 say?"
- "Find the PAC about proposal types"
- "List PACs"

The skill fetches the PAC from the local `.github` clone if available, otherwise from GitHub.

## Structure

Each skill lives in `skills/<skill-name>/` and contains:

- `SKILL.md` — the standard skill definition read by the agent
- `README.md` — human-friendly overview
- Optional `templates/` directory for proposal templates

## License

CC0-1.0
