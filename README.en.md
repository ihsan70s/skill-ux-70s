# Skill UX 70s

[Bahasa Indonesia](README.md) · English

Design user flows, shadcn/ui layouts, screen states, and interface copy for code implementation or Figma.

## Install through your AI agent

Paste this prompt into your agent's chat while your target project is open.

```text
Install Skill UX 70s in this project for the AI agent I am using. Run the command below, select this agent, and verify that skill-ux-70s is installed.

npx skills add ihsan70s/skill-ux-70s --skill skill-ux-70s
```

The repository is private. The GitHub account used for installation needs access.

## Install from a terminal

`npx skills` requires Node.js 22.20 or later. Run the command for your agent from the target project folder.

**Codex**

```sh
npx skills add ihsan70s/skill-ux-70s --skill skill-ux-70s --agent codex
```

**Claude Code**

```sh
npx skills add ihsan70s/skill-ux-70s --skill skill-ux-70s --agent claude-code
```

**Gemini CLI**

```sh
npx skills add ihsan70s/skill-ux-70s --skill skill-ux-70s --agent gemini-cli
```

Add `--global` to install the skill across projects. For another supported agent, omit `--agent` and select your agent when prompted.

### Install from a local copy

If the `skill-ux-70s` folder is next to your target project, run this from the target project. Adjust the path and agent as needed.

```sh
npx skills add '../skill-ux-70s' --skill skill-ux-70s --agent codex --copy
```

[Skills CLI documentation](https://github.com/vercel-labs/skills#install-a-skill)

## Install manually in Codex

1. Create `.agents/skills/skill-ux-70s` in the project root. For all your Windows projects, use `%USERPROFILE%\.agents\skills\skill-ux-70s`.
2. Copy `SKILL.md`, `agents/`, and `references/` into that folder.
3. Open the project in Codex and invoke `$skill-ux-70s`. If the skill does not appear, restart Codex.

## Example prompt

For a new feature or page, the skill uses the existing PRD or drafts one from your brief before designing the UX. It also shares a [ready-to-use PRD prompt](references/prd.md).

```text
Use Skill UX 70s to design a product list with shadcn/ui components.
Include flows for adding, editing, and deleting products, with confirmation and error states.
```

In Codex you can also invoke `$skill-ux-70s`. The skill writes PRDs, UX specifications, and chat questions in Indonesian. Interface copy follows the product's specified language. Creating or editing a Figma file directly requires a Figma integration.

[Official Codex documentation for local skills](https://learn.chatgpt.com/docs/build-skills#where-codex-loads-local-skills)
