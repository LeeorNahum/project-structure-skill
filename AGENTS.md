# AGENTS.md

Rules for editing the **project-structure** skill. User-facing structure rules live in `SKILL.md` and `references/`.

## Editing protocol

- Ask before touching each file; pause for review between files.
- Encode defaults only when backed by usage or explicit user preference.
- Prefer deletion over caveats.

## File roles

| File | Role |
| ------ | ------ |
| `SKILL.md` | Trigger, shapes, verdict format, reference loading |
| `references/definitions.md` | Canonical terms — single owner |
| `references/*.md` | Conditional rules per boundary or folder type |
| `assets/` | Copyable templates |
| `README.md` | Short human summary |

One owner per rule. Elsewhere: use the term or shape, do not restate the rule.

## Wording

- **Opinionated and explicit** on structure — naming patterns, layouts, and boundaries should be stated clearly.
- **Match depth to the reference** — shared files stay short; folder-type references with workflow rules stay fully explicit.
- **Modular ownership** — `SKILL.md` routes and summarizes; each reference owns the detailed rules for its folder type.
- **Preserve crafted phrasing** — when updating a mature reference, change only the wording required by the new rule.
- **Definitions over lists** — terms live in `definitions.md`; prose uses placeholders, not real project names.
- **Positive rules** — state what to do. Avoid negative-anchor phrasing that names the failure mode (see anti-backrooms-design).
- **Concise** — if two sections agree, keep one.
- **Explicit where it matters** — file roles, Git actions, shape trees, template paths.

## Navigation

Reference loading paths belong in `SKILL.md` once. Other files assume the agent already loaded what that section requires.

## Before finishing

- Reference loading covers each `references/` file.
- Terms in references appear in `definitions.md`.
- Bump `metadata.version` when behavior changes.
