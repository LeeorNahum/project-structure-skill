# Brand Folder

`Brand/` is an **organizer folder** for visual identity work. Not a repo boundary.

## Brand Folder Shape

```text
Brand/
└── <Project-or-Surface>-Brand/
    ├── Icon/
    └── Logo/
```

The canonical deliverable sits directly under `Brand/` using `<Project-or-Surface>-Brand/` naming as the default pattern, following the same organizer/deliverable rule as elsewhere in this skill. Prefer the smallest specific name that clearly identifies the branded surface or project.

Subfolders inside the brand deliverable use short scoped names (`Icon/`, `Logo/`, `Colors/`, `Banners/`) since the project or brand surface identity is already carried by the parent.

Reference material may be committed alongside final assets when it belongs to the deliverable. Cleanup is a future commit judgment call, not a rule.

## Rules

- No Git on `Brand/` itself
- Git on the brand deliverable folder only when the user requests it
- Remote only when the folder name is standalone-meaningful on GitHub (see `repo-boundaries.md`)
