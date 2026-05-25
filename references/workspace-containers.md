# Workspace Containers

A **workspace container** holds mixed local work, optional nested repos, and sometimes installed agent skills.

## Layout

```text
Project Name/
├── AGENTS.md
├── README.md
├── .gitignore
├── .gitmodules
└── .agents/
    └── skills/
```

## Defaults

- Git locally only; no remote by default
- Skills under `.agents/skills/` when needed
- Track root operating docs, `.gitmodules`, and skill gitlinks
- Ignore contained work folders by default
- No Git on organizer folders unless the user asks
- Canonical deliverable folders may own their own repos when justified
- Add folders only when they hold real content

`.gitignore`: start from `assets/gitignore-workspace-container.template`.

## Root docs

- `README.md` — human-facing, short, stable
- `AGENTS.md` — agent navigation, skills, Git posture
- `TASKS.md` — only if this container owns durable execution state

Do not turn root docs into a folder inventory.

## Skills

Submodule installs require a Git repo at the container root. That does not make child folders publishable.

Install at the container when the whole workspace inherits the skill; install in a subproject when the guidance is local to that repo only.
