# Definitions

Canonical terms for this skill. Define once here; use the term elsewhere without redefining it. Git and remote defaults live only in `repo-boundaries.md`.

## Workspace container

The named project root the user opens day to day. Holds mixed local work and optional nested repos. May use a local Git repo for root operating docs, `.gitmodules`, and skill submodules only. Not the publishable product repo.

## Full project root

A project root with multiple real surfaces already in active use — planning, web, firmware, brand, devices, or similar. Not scaffolding; not the same as a workspace container that mainly coordinates subprojects.

## Organizer folder

A folder whose name describes a **category**, not one deliverable. Too broad to be understood as a repository title without extra context.

## Canonical deliverable folder

A folder whose name is specific enough to be understood as a repository title, usually `<Project> <Deliverable>` or a deployable slug. It is the canonical home for one shippable, versionable, or durable unit.

It may live inside an organizer folder. Being repo-ready by name does not mean it must sit at the workspace root or receive Git automatically.

## Shape

The durable folder layout for one repo or workspace boundary. Pick the smallest shape that fits.
