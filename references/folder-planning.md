# Planning Folder

`Planning/` is an **organizer folder** for durable thinking, notes, constraints, and context that does not belong inside a separate repo for finalized deliverables.

Skip `Planning/` when a short `README.md` section is enough.

Planning repos use this shape:

```text
Planning/
└── Project-Plan/
    ├── AGENTS.md
    ├── README.md
    ├── TASKS.md
    └── docs/
        └── <topic>/
        └── <topic>/
        └── <topic>/
```

`Project-Plan/` is the canonical deliverable folder. `README.md` owns project purpose, strategy, scope, and human-readable context. `TASKS.md` owns executable state. Topic folders under `docs/` should be created, renamed, split, merged, or removed as the plan evolves.

Planning is encouraged to be broad. It can have many folders, subfolders, and markdown files when the project needs them. The constraint is not the number of files; the constraint is whether each file has a clear purpose, stays concise, and avoids duplicating facts that can drift.

Create only the subfolders that have real files now, but do not treat the first folder layout as permanent. Planning should always be freely reorganized as understanding improves.

## Planning AGENTS.md

For non-trivial planning folders, add or update `Planning/AGENTS.md`. It should explain how that planning folder is organized, which files own durable facts, and how future agents should keep the folder clean and avoid duplication or knowledge drift as the project changes.

Maintenance behavior:

- Keep documentation files modular and purposeful
- Move, rename, split, merge, and recategorize when structure drifts
- Remove stale or duplicated facts instead of preserving them forever
- Promote executable state to `TASKS.md`; promote stable repo guidance to `AGENTS.md`

Workflow rules:

- Create a new markdown file for a new durable topic instead of appending everything to one large note.
- Use descriptive file names that say what the file is about.
- Move, rename, split, merge, and recategorize files when the current organization stops matching the project.
- Keep folders and filenames descriptive rather than treating any initial category set as sacred.
- Do not duplicate the same factual content in multiple files; update the owning file and link to it if necessary.
- If a note is executable state, use `TASKS.md`; if it is stable repo guidance, use `AGENTS.md`.

Avoid turning planning into a dumping ground. Modularity should make the project easier to resume, not harder to navigate. Clean or prune stale, redundant, or miscategorized notes instead of preserving them out of inertia.

A planning repo lives at `Planning/Project-Plan/`.
