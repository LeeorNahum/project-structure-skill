# Firmware Folder

Use `Firmware/` when a project root contains embedded firmware as a serious surface, especially when the firmware may become its own repo.

## Observed Pattern

```text
Project Name/
└── Firmware/
    └── <Project-or-Surface>-Firmware/
```

Use `<Project-or-Surface>-Firmware/` naming as the default pattern, following the same organizer/deliverable rule as elsewhere in this skill. Prefer the smallest standalone-meaningful firmware artifact name that matches the actual deliverable.

## PlatformIO Repo Shape

Inside a canonical deliverable PlatformIO firmware repo, a common shape is:

```text
<canonical-firmware-repo>/
├── platformio.ini
├── hardware/
├── src/
└── lib/
```

Use the repo's existing firmware conventions before introducing new ones.

For a minimal PlatformIO `.gitignore`, start from `assets/gitignore-firmware-platformio.template`, then adjust only for the repo's actual generated files and intentionally tracked editor settings.

This reference covers only creating the folder. For board environments, hardware selectors, build flags, versioning, library dependencies, provisioning, and local values, install and follow the [`firmware-repository-opinions`](https://github.com/LeeorNahum/firmware-repository-opinions-skill) skill. Expansion beyond creating the folder is owned by that skill.
