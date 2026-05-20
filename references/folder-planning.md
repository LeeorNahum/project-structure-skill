# Planning Folder

Use `Planning/` when a project has durable thinking, notes, constraints, context, or organization that does not belong inside one code or device repo.

Do not create `Planning/` for a tiny repo that only needs a short `README.md` section.

Planning is allowed to be broad. It can have many folders, subfolders, and markdown files when the project needs them. The constraint is not the number of files; the constraint is whether each file has a clear purpose, stays concise, and avoids duplicating facts that can drift.

Create only the subfolders that have real files now, but do not treat the first folder layout as permanent. Planning should be reorganized as understanding improves.

## Planning AGENTS.md

For non-trivial planning folders, add or update `Planning/AGENTS.md`. It should explain how that planning folder is organized, which files own durable facts, and how future agents should keep the folder clean as the project changes.

`Planning/AGENTS.md` should reinforce maintenance behavior:

- keep markdown files modular and purposeful
- move, rename, split, merge, and recategorize notes when the structure drifts
- remove stale or duplicated facts instead of preserving them forever
- link to the owning file instead of restating the same fact in multiple places

Workflow rules:

- Create a new markdown file for a new durable topic instead of appending everything to one large note.
- Use descriptive file names that say what the file is about.
- Move, rename, split, merge, and recategorize files when the current organization stops matching the project.
- Keep folders and filenames descriptive rather than treating any initial category set as sacred.
- Keep meeting/event/raw notes separate until a durable decision or task is promoted.
- Do not duplicate the same factual content in multiple files; update the owning file and link to it.
- If a note is executable state, use `TASKS.md`; if it is stable repo guidance, use `AGENTS.md`.

Avoid turning planning into a dumping ground. Modularity should make the project easier to resume, not harder to navigate. Clean stale, redundant, or miscategorized notes instead of preserving them out of inertia.
