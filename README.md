# Cloudsmith Marketing Skills

A shared library of Claude skills for the Cloudsmith marketing team. Each `.skill` file gives
Claude precise, team-specific instructions for a recurring task — so anyone on the team gets
consistent, on-brand output without having to re-explain context every time.

---

## How to use a skill

1. Open Claude (Cowork desktop app or claude.ai)
2. Make sure your Skills folder is connected to this repo (or copy the `.skill` file into your
   local Claude Workspace/Skills folder)
3. Just describe what you want in plain language — Claude will recognise the task and follow
   the skill automatically

You don't need to say "use the skill" or reference it by name. Just start the task naturally.

---

## Available skills

| Skill file | What it does | Trigger phrases |
|---|---|---|
| `cloudsmith-skill-builder.skill` | Builds a new skill from scratch and saves it to your Skills folder | "Build me a skill for…", "Create a new skill that…", "I want a skill to…" |
| `cloudsmith-content-calendar.skill` | Generates a full week of social media posts (LinkedIn + X) as a downloadable CSV | "Create a content calendar", "Generate posts for this week", "Let's do the social calendar" |

---

## Adding a new skill

The easiest way to build a new skill is to use the **skill builder skill** — it guides you
through the process and packages the output automatically.

Just say: *"Build me a skill for [task]"*

Claude will ask you a series of questions, write the SKILL.md, and save the packaged `.skill`
file to your Skills folder. You then commit it to this repo so the whole team can use it.

To add it manually:
1. Create a folder: `your-skill-name/`
2. Add a `SKILL.md` inside it following the format of existing skills
3. Zip the folder: `zip -r your-skill-name.skill your-skill-name/`
4. Add the `.skill` file to the root of this repo
5. Update the table above with the skill name, description, and trigger phrases
6. Commit and push

---

## Updating an existing skill

1. Unzip the `.skill` file: `unzip your-skill-name.skill`
2. Edit the `SKILL.md` inside
3. Rezip: `zip -r your-skill-name.skill your-skill-name/`
4. Commit with a short note describing what changed (e.g. "added funnel stage question to intake")
5. Team members pull the latest and replace their local copy

---

## Skill format reference

Each `.skill` file is a zip archive containing at minimum:

```
your-skill-name/
└── SKILL.md        ← instructions Claude reads and follows
```

Optionally:

```
your-skill-name/
├── SKILL.md
└── references/
    ├── voice-and-style.md
    └── [any supporting reference files]
```

The `SKILL.md` starts with a YAML frontmatter block:

```yaml
---
name: your-skill-name
description: >
  One paragraph describing what the skill does and when to trigger it.
  Include natural trigger phrases so Claude auto-activates at the right time.
---
```

---

## Questions or issues?

Post in [#team-marketing](https://cloudsmith.slack.com) or reach out to Juliana.
