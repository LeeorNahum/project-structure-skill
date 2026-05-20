# Workspace Containers

A workspace container is a human-readable folder that helps the user live inside a project with many surfaces. It may contain real repos, local-only folders, assets, exports, notes, and installed agent skills.

The container can be Git-initialized without becoming a publishable project. Treat that Git repo as a local control plane.

## Default Strategy

Use this pattern when the user opens a main folder that contains many subfolders and wants skills installed as submodules:

```text
Project Name/
├── AGENTS.md
├── README.md
├── .gitignore
├── .gitmodules
└── .agents/
    └── skills/
```

Default behavior:

- initialize Git locally only
- add no remote by default
- install shared local skills under `.agents/skills/` only when the project needs local skill files
- track `.gitmodules`, skill submodule gitlinks, and a few root operating docs
- ignore contained project folders by default
- let serious subprojects own their own Git repos when justified
- add content folders only when they hold real project material

When creating the parent `.gitignore`, start from `assets/gitignore-workspace-container.template`.

## Local Control Plane Git

Use a local control-plane repo when:

- skills need to be installed as Git submodules
- the container needs `AGENTS.md`, `README.md`, or root standards
- the user wants Cursor/VSCode open at the main folder
- contained subprojects are not all meant to be committed together

Do not add a GitHub remote unless the user explicitly wants the container's root standards synced or backed up. If a remote is added, default to private and keep the deny-all ignore shape.

## Root Docs

Use root docs sparingly:

- `AGENTS.md`: how agents should navigate the workspace, which skills are installed, and what must stay local
- `README.md`: canonical purpose, surfaces, current active subprojects, setup, and non-goals
- `TASKS.md`: only if the container itself owns durable execution state

Do not turn the root docs into an exhaustive inventory. Link to subproject docs instead.

## Skill Installation

For local skill installs, prefer `.agents/skills/<skill-name>/`.

If installed as submodules, the container must be a Git repo. This does not mean the container should publish its child folders.

Do not install a skill repo just because a raw URL or explicit user-provided reference was enough for the current task.

If nested subprojects also need the skill, prefer one of these:

- install the skill at the container root when the whole workspace should inherit it
- install a subproject-specific skill inside that subproject when the guidance only applies there
- avoid duplicate installs unless the child repo must work independently outside the container
