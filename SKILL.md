---
name: project-structure
description: Choose and normalize opinionated project, workspace, and repo structure. Always use when setting up, scaffolding, reorganizing, splitting, auditing, naming, git-initializing, or publishing a project; deciding whether a folder is a local workspace container, planning repo, full project root, web/app repo, firmware/library repo, or canonical publishable repo; installing local skills; or creating root docs and gitignore boundaries.
metadata:
  author: Leeor Nahum
  version: "2.4.0"
---

# Project Structure

Classify the project before creating structure. The right folder shape should make the work easier to inhabit, not just look organized.

Prefer the smallest durable shape that can ship the project. Do not create planning folders, `.gitkeep` placeholders, extra directories, or task files just because a project is new.

Use the user's actual project boundary, not the folder that happened to be open. A main workspace folder can be a local control plane for many subprojects without being a publishable repo itself.

## Reference Loading

Read the relevant reference before acting:

- Read `references/definitions.md` first when classifying folders, naming, or choosing doc roles.
- Read `references/workspace-containers.md` when a main folder contains many subfolders/repos, when installing skills as submodules, or when deciding whether the container itself should be Git-controlled.
- Read `references/repo-boundaries.md` before initializing Git, adding a remote, naming a repo, or deciding whether a subfolder deserves GitHub.
- Read the matching folder reference before creating one of these folders: `references/folder-planning.md`, `references/folder-web.md`, `references/folder-firmware.md`, `references/folder-devices.md`, or `references/folder-brand.md`.

Use `assets/` only for copyable templates or static resources that are intentionally meant to become files in another project. If an asset is not a close fit, ask before using it.

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

### Workspace Container / Local Control Plane

Use for a human-readable folder that contains many related subfolders, some of which are independent repos and some of which are local-only work areas.

```text
Project Name/
├── AGENTS.md
├── README.md
├── .gitignore
├── .gitmodules
└── .agents/
    └── skills/
```

Default strategy: initialize Git locally only so submodule-installed skills can exist, add no remote by default, and use a deny-all `.gitignore` that tracks only root operating docs, `.gitmodules`, and skill submodule entries.

Do not treat contained folders as publishable just because the container is Git-controlled. A nested canonical deliverable folder may live inside an organizer and still become its own repo when justified.

Do not create content folders in the container example just to suggest future structure. Add folders only after the project proves it needs them.

### Minimal Artifact Or Package Repo

Use for a single releaseable artifact such as a theme, preset, config package, template, small asset pack, downloadable zip, or other repo where the artifact is the product.

```text
project-name/
├── AGENTS.md
├── README.md
├── <artifact-folder>/
└── <minimal build/package script if needed>
```

Only add folders that hold real files now. Skip `TASKS.md`, `docs/`, `decisions/`, `resources/`, and `.gitkeep` files unless the user asked for them or the artifact already needs them.

If unsure whether a project is a planning repo or a minimal artifact repo, ask before creating structure. Default to minimal when the immediate goal is "make/publish/install this thing."

### Planning Repo

Use when the project is still being designed but already has product, software, hardware, or decision material.

`Planning/` is the organizer. `Project-Plan/` is the canonical deliverable folder. Read `references/folder-planning.md` for the exact layout and maintenance rules.

### Full Project Root

Use when a project spans multiple serious surfaces such as web/app, firmware, devices, brand assets, planning, or public packaging. This is not hardware-only; hardware projects are just the clearest example.

```text
Project Name/
├── AGENTS.md
├── Planning/
├── Web/
├── Firmware/
├── Devices/
└── Brand/
```

Only create folders that correspond to real surfaces. Keep planning, code, devices, brand assets, and generated artifacts separate. Give serious canonical deliverable folders their own `AGENTS.md`.

If the root mainly exists to hold subprojects and shared agent standards, prefer the workspace container shape above.

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

When PlatformIO hardware selectors, board environments, local provisioning values, or firmware version flags matter, also use the firmware-specific repository skill if available.

## Naming

Classify with defined terms. Git and remote rules are in `repo-boundaries.md`.

- Human-readable local roots: `Project Name`
- Deployable code slugs: `project-<surface>`
- Planning repos live under `Planning/Project-Plan/`
- Avoid names that describe temporary process unless that is the artifact's identity

## First Files

Every non-trivial project starts with the minimum files that fit its shape.

- `AGENTS.md` — agent operating rules
- `README.md` — human-facing summary
- `TASKS.md` — executable state when the repo needs durable task tracking

One owner per fact. Do not duplicate rules across files.

For workspace containers, `AGENTS.md` covers navigation, skills, and Git posture — not a folder inventory.

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
- Do not over-apply this skill by scaffolding future folders. Structure should prove it is needed by holding real project content.
- Do not add a GitHub remote just because Git exists locally.
- Do not publish non-canonical scratch folders unless the user explicitly confirms the exception.
- Do not duplicate the same standard across multiple files; put the durable rule in one owner and link to it.
- Ask before git commit, push, or GitHub release unless the user already approved that specific action.
