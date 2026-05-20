# Devices Folder

Use `Devices/` when a project root contains one or more hardware/device design repos or device-specific source folders.

Observed pattern:

```text
Project Name/
└── Devices/
    └── <Canonical Device Or Board Repo>/
```

The child folder can be its own Git repo when it is a real publishable or durable device artifact. Do not make the parent root track the child repo's files by accident.

Use the canonical product/device name in the child folder when the device artifact is meant to stand alone. Add revision or surface wording only when it clarifies the artifact's identity.

Do not invent deeper device subfolders before the project shows a need. Source files, libraries, vendor outputs, CAD files, or manufacturing packages should follow the actual tool and project evidence.

For a KiCad PCB repo `.gitignore`, start from `assets/gitignore-kicad-pcb.template`. Before ignoring an unfamiliar physical-design file extension, verify whether it is source, cache, or deliverable.

Ask before:

- turning a device folder into a GitHub repo
- renaming a device or board folder
- splitting one device into multiple repos
- adding generic physical-design folders that are not already used by the project
