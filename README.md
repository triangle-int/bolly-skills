# Bolly Skills Registry

Community skills for [Bolly](https://github.com/triangle-int/bolly) — teach your companion new abilities.

## Browse

Visit [bolly.triangleint.com/skills](https://bolly.triangleint.com/skills) to browse available skills.

## Publishing a skill

1. Create a GitHub repo with:
   - `skill.json` — manifest with `id`, `name`, `description`, `icon`
   - `instructions.md` — the prompt fragment injected into your companion

2. Open a PR to this repo adding your skill to `registry.json`:

```json
{
  "id": "your-skill-id",
  "name": "Your Skill Name",
  "description": "What this skill teaches your companion to do.",
  "icon": "~",
  "repo": "your-username/your-skill-repo",
  "git_ref": "main",
  "author": "Your Name"
}
```

## Skill format

### `skill.json`

```json
{
  "id": "code-reviewer",
  "name": "Code Reviewer",
  "description": "Reviews code for bugs, style issues, and improvements.",
  "icon": "~",
  "enabled": true
}
```

### `instructions.md`

A markdown file containing the prompt fragment that gets injected into the companion's system prompt when the skill is active. Write it as if you're teaching the companion a new behavior.

## Installing skills

From your Bolly instance's Skills tab, switch to **Browse** and click **Install** on any skill. Or install manually:

```
# Skills are stored in ~/.bolly/skills/{skill-id}/
```
