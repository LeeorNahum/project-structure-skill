# Definitions

Canonical terms for this skill. Define once here; use the term elsewhere without redefining it. Git and remote defaults live only in `repo-boundaries.md`.

## Workspace Container

The named project root the user opens day to day. Holds mixed local work and optional nested repos. May use a local Git repo for root operating docs, `.gitmodules`, and skill submodules only. Not the publishable product repo.

## Full Project Root

A project root with multiple real surfaces already in active use: planning, web, firmware, brand, devices, or similar. Not scaffolding; not the same as a workspace container that mainly coordinates subprojects.

## Organizer Folder

A folder whose name describes a **category**, not one deliverable. Too broad to be understood as a repository title without extra context.

## Canonical Deliverable Folder

A folder whose name is specific enough to be understood as a repository title, usually `<Project> <Deliverable>` or a deployable slug. It is the canonical home for one shippable, versionable, or durable unit.

It may live inside an organizer folder. Being repo-ready by name does not mean it must sit at the workspace root or receive Git automatically.

## Shape

The durable folder layout for one repo or workspace boundary. Pick the smallest shape that fits.

## Planning Docs Folder

In a planning repo, `Docs/` is the active plan folder. It holds the current implementation guidance as Title Case topic folders and markdown files. It is not a generic documentation dump and it is not wrapped by another "active plan" folder.

## Deprecated Planning Docs Folder

In a planning repo, optional sibling folder next to `Docs/` that preserves superseded planning material for reference only. Agents ignore it for implementation unless the user explicitly asks for historical context.

## Title Case

Capitalization style for planning folder and markdown filenames. Capitalize principal words, including the first and last words. Lowercase articles, short prepositions, and common conjunctions unless they are first or last. See [Title case](https://en.wikipedia.org/wiki/Title_case).

## Title-Dash-Case

Capitalization style for canonical deliverable folder names and repo folder names that use multiple words joined by hyphens. Capitalize the first letter of each word segment. Examples: `My-App`, `Project-Firmware`. Use this for the filesystem folder name and repo title only. Do not use it for npm package names, import paths, source directories, or code identifiers, which remain kebab-case.
