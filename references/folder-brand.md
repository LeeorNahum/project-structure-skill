# Brand Folder

`Brand/` is an **organizer folder** for visual identity work. Not a repo boundary.

## Brand Folder Shape

```text
Brand/
└── <Project>-Brand/
    ├── Icon/
    └── Logo/
```

The canonical deliverable sits directly under `Brand/` using `<Project>-Brand/` naming, following the same organizer/deliverable pattern used throughout this skill.

Subfolders inside `<Project>-Brand/` use short scoped names (`Icon/`, `Logo/`, `Colors/`, `Banners/`) since the project prefix is already carried by the parent.

Reference material such as source PNGs or working files may be committed alongside final assets. Cleanup is a future commit judgment call, not a rule.

## Rules

- No Git on `Brand/` itself
- Git on `<Project>-Brand/` only when the user requests it
- Remote only when the folder name is standalone-meaningful on GitHub (see `repo-boundaries.md`)

## Ask Before

Ask before renaming assets, splitting asset types into separate repos, or mixing unrelated brand assets into the same folder.
