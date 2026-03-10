# Bolly Skills Registry

Community skills for [Bolly](https://github.com/triangle-int/bolly) — teach your companion new abilities.

Skills follow the open [Agent Skills](https://agentskills.io) standard (`SKILL.md`).

## Browse

Visit [bolly.triangleint.com/skills](https://bolly.triangleint.com/skills) to browse available skills.

## Adding a skill to the registry

Open a PR adding an entry to `registry.json`. Skills can live in any GitHub repo — this registry just points to them.

```json
{
  "id": "your-skill-id",
  "name": "Your Skill Name",
  "description": "What this skill teaches your companion to do.",
  "icon": "~",
  "repo": "your-username/your-repo",
  "git_ref": "main",
  "author": "Your Name",
  "path": "skills/your-skill"
}
```

| Field | Required | Description |
|-------|----------|-------------|
| `id` | yes | Unique skill identifier |
| `name` | yes | Display name |
| `description` | yes | What the skill does |
| `icon` | no | Single character icon |
| `repo` | yes | GitHub repo (`owner/repo`) |
| `git_ref` | no | Branch or tag (default: `main`) |
| `author` | no | Author display name |
| `path` | no | Subdirectory within the repo containing `SKILL.md` |

## Skill format

Each skill directory needs a `SKILL.md` file with YAML frontmatter:

```markdown
---
name: your-skill
description: What this skill does and when to use it.
---

Instructions for the companion...
```

See the full spec at [agentskills.io/specification](https://agentskills.io/specification).

## Installing skills

From your Bolly instance's Skills tab, switch to **Browse** and click **Install**.
