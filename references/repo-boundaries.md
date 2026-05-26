# Repo Boundaries

Git is not the same decision as GitHub.

Most folders should have **no Git**. Do not init Git because a folder has files or because an ancestor is Git-controlled.

## Classify First

Before init, remote, rename, or publish: classify the folder using defined terms in `definitions.md`.

| Kind | Git | Remote |
|------|-----|--------|
| Organizer folder | No | No |
| Canonical deliverable folder | Only when justified | Only if user requests |
| Workspace container | Local control plane | Rare; ask first |
| Scratch / temp / import | No | No |

Local Git outside a control plane is uncommon. Use it when history, collaboration, releases, submodules, or explicit user request clearly need it.

## Remote

Suggest a remote only when the folder is a **canonical deliverable folder**, has a durable purpose, and the user wants sync, collaboration, CI, releases, or backup.

The folder name must be standalone-meaningful as a GitHub repo name without extra context. Generic names like `Assets`, `Docs`, `Config`, or single category words that describe a role rather than a deliverable are not standalone-meaningful and should not get a remote. Names that include the project identity, surface, and optionally a type are standalone-meaningful. Names that are generic category words are not.

The local folder name and the GitHub repo name must match. If they would differ, either rename the local folder to match or do not create the remote.

Do not suggest a remote because the parent is Git-controlled, the folder contains files, or the agent wants somewhere to commit.

## Nested Repos

- Parent control plane tracks root docs, `.gitmodules`, and skill gitlinks, not child contents.
- Child repos track their own source and release artifacts.
- Child repos that must work alone get their own `AGENTS.md`.

## Before Acting

```text
Classify: organizer, canonical deliverable, or workspace container?
If remote: should this name exist on GitHub, and public or private?
If unclear: no Git, no remote.
```

Ask before publishing names tied to temporary process, tooling residue, or unclear identity.

## Git Actions

Ask before commit, push, or GitHub release unless the user already approved that specific action. Show the diff first.
