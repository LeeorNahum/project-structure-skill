# Planning Folder

`Planning/` is an **organizer folder** for durable thinking, notes, constraints, and context that does not belong inside a separate repo for finalized deliverables.

A planning repo lives at `Planning/Project-Plan/`.

## Planning Repo Shape

```text
Planning/
└── Project-Plan/
    ├── AGENTS.md
    ├── README.md
    ├── Docs/
    │   ├── <Document>.md
    │   ├── <Document>.md
    │   └── <Topic>/
    │       └── <Document>.md
    └── Deprecated/          (optional; only when old material must be kept)
        ├── <Archived Document>.md
        ├── <Archived Document>.md
        └── <Archived Topic>/
            └── <Archived Document>.md
```

`Project-Plan/` is the canonical deliverable folder. `README.md` owns project purpose, strategy, scope, and human-readable context. Topic folders under `Docs/` should be created, renamed, split, merged, or removed as the plan evolves.

Planning is encouraged to be broad. It can have many folders, subfolders, and markdown files when the project needs them. The constraint is not the number of files; the constraint is whether each file has a clear purpose, stays concise, and avoids duplicating facts that can drift.

## `Docs/` Is the Active Plan

`Docs/` is the active plan. Do not add a wrapper folder inside it.

Do not put planning markdown in the repo root beyond `AGENTS.md` and `README.md`.

`Deprecated/` is a sibling of `Docs/`, not nested inside it. Add it only when superseded material must be preserved for reference. Agents must treat `Deprecated/` as non-guidance and ignore it for implementation unless the user explicitly asks for historical context.

Create any topic folders and subfolders that will have real files now, but do not treat the first folder layout as permanent. Planning should always be freely reorganized as understanding improves and the project evolves. Rename, split, merge, or remove them as the plan evolves.

## Naming Conventions

Use [Title Case](https://en.wikipedia.org/wiki/Title_case) for planning folder and markdown filenames. Capitalize the principal words, including the first and last. Articles (`a`, `an`, `the`), short prepositions, and common conjunctions are lowercase unless first or last.

Do not use lowercase folder names, kebab-case filenames, or snake_case filenames unless an external tool requires it.

Keep folders and filenames descriptive rather than treating any initial category set as sacred.

## Markdown Frontmatter

Every planning markdown file must start with YAML frontmatter:

```yaml
---
name: <Title Case Document Name>
description: <one-line sentence describing the file>
date_created: YYYY-MM-DD
date_modified: YYYY-MM-DD
---
```

The `description` value must be a single sentence on one line.

Keep frontmatter in sync with the file:

- `name` matches the current document name
- `description` matches the current purpose of the file
- `date_created` stays fixed after the file is created
- `date_modified` updates whenever the file content changes

## One Topic Per File

Prefer more markdown files over fewer combined files.

Create a new markdown file when a topic is distinct enough to implement, review, or update on its own.

Do not combine unrelated topics into one file just to reduce file count. Split when a file covers multiple implementation areas that would naturally live in different folders.

Keep a file together only when the content is one coherent topic with no meaningful split point.

Create a new markdown file for a new durable topic instead of appending everything to one large note.

Use descriptive file names that say what the file is about.

## Maintenance

- Keep documentation modular and purposeful
- Move, rename, split, merge, and recategorize when structure drifts
- Remove stale or duplicated facts instead of preserving them forever
- Do not duplicate the same factual content in multiple files; update the owning file and link instead

Avoid turning planning into a dumping ground. Modularity should make the project easier to resume, not harder to navigate. Clean or prune stale, redundant, or miscategorized notes instead of preserving them out of inertia.

## Planning AGENTS.md

For non-trivial planning folders, add or update `AGENTS.md`. It should explain how the planning repo is organized, which files own durable facts, and how future agents should keep the folder clean and avoid duplication or knowledge drift as the project changes.
