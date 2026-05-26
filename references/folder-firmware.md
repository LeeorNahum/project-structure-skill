# Firmware Folder

Use `Firmware/` when a project root contains embedded firmware as a serious surface, especially when the firmware may become its own repo.

## Observed Pattern

```text
Project Name/
└── Firmware/
    ├── AGENTS.md
    └── <Canonical Firmware Repo>/
```

## PlatformIO Repo Shape

Inside a canonical deliverable PlatformIO firmware repo, a common shape is:

```text
<canonical-firmware-repo>/
├── platformio.ini
├── hardware/
├── src/
└── lib/
```

Use the repo's existing firmware conventions before introducing new ones. If there is a dedicated firmware-configuration skill or repo-local `AGENTS.md`, follow that for board environments, hardware selectors, build flags, provisioning, and version constants.

For a minimal PlatformIO `.gitignore`, start from `assets/gitignore-firmware-platformio.template`, then adjust only for the repo's actual generated files and intentionally tracked editor settings.

## Ask Before

- Changing board targets or upload defaults
- Changing hardware selectors, pin maps, or firmware identity
- Moving firmware into or out of its own repo
- Adding generated build folders to Git
