---
name: project-structure-chooser
description: Choose and normalize opinionated project/repo structure. Use when starting, reorganizing, splitting, or auditing a project; deciding between planning repo, full project root, web/app monorepo, firmware/library repo, artifact snapshot, or event deliverable; or creating the minimum durable files for the chosen shape.
metadata:
  author: Leeor Nahum
  version: "1.0.0"
---

# Project Structure Chooser

Classify the project before creating structure. The right folder shape should make the work easier to inhabit, not just look organized.

## Verdict First

Start with a short verdict:

```text
Recommended shape: <shape>
Why: <one sentence>
First files: <files>
First three tasks: <tasks>
```

Then give the folder shape and any caveats.

## Shapes

### Small Planning Repo

Use for tiny, early, or spec-only projects.

```text
Project-Plan/
├── AGENTS.md
├── PROJECT.md
└── TASKS.md
```

Graduate when decisions, research, meetings, code, hardware, or media no longer fit cleanly in root files.

### Planning Repo

Use when the project is still being designed but already has product/software/hardware/research decisions.

```text
Project-Plan/
├── AGENTS.md
├── PROJECT.md
├── TASKS.md
├── docs/
│   ├── product/
│   ├── software/
│   ├── hardware/
│   ├── research/
│   └── decisions/
└── meetings/
```

`PROJECT.md` owns strategy and scope. `TASKS.md` owns executable state. Stable decisions move into `docs/decisions/`.

### Full Project Root

Use when a project spans multiple serious surfaces such as planning, web/app, firmware, hardware, devices, assets, presentation, research, or public packaging. This is not hardware-only; hardware projects are just the clearest example.

```text
Project Name/
├── AGENTS.md
├── Planning/
├── Firmware/
├── Web/
├── Devices/
├── Assets/
├── Presentation/
└── Research/
```

Only create folders that correspond to real surfaces. Keep planning, code, devices, media, and presentation artifacts separate. Give serious subprojects their own `AGENTS.md`.

### Web/App Monorepo

Use for deployable TypeScript web, app, extension, or service surfaces.

```text
project-slug/
├── AGENTS.md
├── apps/
├── packages/
├── docs/
└── package.json
```

Add `TASKS.md` only when the repo needs durable executable state. Do not require it for small web apps or extensions by default.

### Firmware Or Library Repo

Use for PlatformIO firmware, reusable C++ libraries, BLE/OTA/sensor packages, or hardware abstraction code.

```text
firmware-library/
├── AGENTS.md
├── README.md
├── platformio.ini
├── include/
├── src/
├── lib/
├── hardware/
├── examples/
├── test/
└── docs/
```

Add `TASKS.md` only when the repo needs durable executable state.

### Artifact Snapshot

Use for posters, slides, screenshots, CAD exports, 3D prints, media packets, and event deliverables.

```text
Artifact Name YYYY-MM-DD/
├── README.md
├── source/
├── exports/
├── references/
├── screenshots/
├── photos/
└── notes.md
```

Record source files, final export format, public-safe caption/description, and missing media or privacy constraints.

## Naming

- Local project roots can be human-readable: `Project Name`.
- Code repos should use deployable/package slugs: `project-website`, `project-firmware`, `project-skill`.
- Planning repos use `Project-Plan`.
- Keep old date-stamped folders as snapshots unless current work revives them.

## First Files

Every non-trivial project starts with the minimum files that fit its shape.

- `AGENTS.md`: durable agent operating rules for any serious repo
- `PROJECT.md`: canonical purpose, scope, users, and non-goals for planning repos or larger project roots
- `TASKS.md`: executable state for planning repos or larger active projects, not mandatory for every code repo

Do not duplicate facts across files. Update the owning file and link to it.

## First Three Tasks

1. Define one core outcome and one non-goal.
2. Write the smallest useful end-to-end deliverable.
3. Identify manual blockers: credentials, hardware, account owner, photos, domains, API keys.

## Boundaries

- Do not put project history or diary text into `AGENTS.md`.
- Do not use a full project root for a tiny idea unless it has multiple real surfaces.
- Do not collapse related-but-distinct products into one repo just because they share parts.
- Keep shape decisions separate from domain implementation details.
- If a project only needs one subfolder shape, use that shape directly instead of forcing a full product root.
