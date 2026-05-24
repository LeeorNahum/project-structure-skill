# Brand Folder

Use `Brand/` when a project has visual identity assets that should stay organized locally. `Brand/` is a **surface folder** for navigation, not a publishable repo boundary.

Do not initialize Git on `Brand/` itself or treat it as a GitHub repository. A folder named `Brand/` is too generic to stand alone on a profile and does not describe one atomic deliverable.

## Preferred Shape

```text
Brand/
└── Assets/
    ├── <Project> Icon/
    └── <Project> Logo/
```

Use canonical names under `Assets/`:

- `<Project> Icon/` for icon source files and exports
- `<Project> Logo/` for logo source files and exports

These atomic folders carry the project name plus the asset type. That naming signals a standalone scope that *may* become its own Git repo with a remote if the user requests it.

## Git And Remotes

Default: **no Git** on `Brand/`, `Brand/Assets/`, or other surface folders.

Initialize Git only on an atomic asset folder such as `Audiote Icon/` when:

- the user explicitly wants version history or a remote for that asset set
- the folder is the canonical source for that icon, logo, or brand package
- the name is ready to appear as a repo on GitHub

Before adding a remote on an atomic brand folder, ask whether it should be public or private.

Do not suggest remotes for:

- `Brand/`
- `Brand/Assets/`
- undifferentiated media dumps
- temporary mockups or one-off exports

## Naming Rules

- Do not date-stamp folders under `Brand/Assets/`. Names like `<Project> Icon 5.16.2026/` are backup habits, not canonical structure.
- Do not rename or flatten atomic asset folders without asking.
- Keep one-off screenshots, generated presentation exports, and temporary mockups outside `Brand/` unless they become part of the durable identity system.
- For dated deliverable packets or export backups, use an **Artifact Snapshot** folder outside `Brand/`, not a date suffix inside `Brand/Assets/`.

Ask before renaming brand assets, flattening icon/logo folders, or mixing unrelated media into `Brand/Assets/`.
