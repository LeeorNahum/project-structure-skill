# Skill Installation

Local skills are repo-scoped.

Install skills under `.agents/skills/` in the repo whose agents should inherit the guidance.

Read the skill's frontmatter `name` and install it at `.agents/skills/<name>/`. The local directory that directly contains `SKILL.md` must match `name` exactly. Remote repository naming does not determine the installed directory.

When both a parent root and a nested canonical deliverable folder need skills, install skills separately in each repo. Each repo owns its own `.agents/skills/` folder and `.gitmodules`.

Do not install project-specific skills into a global agent skills folder unless the user explicitly asks for a global install.
