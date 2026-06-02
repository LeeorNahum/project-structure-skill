# Skill Installation

Local skills are repo-scoped.

Install skills under `.agents/skills/` in the repo whose agents should inherit the guidance.

Use the source repo folder name as the installed folder name. If the source repo is named `example-skill`, install it as `.agents/skills/example-skill`.

When both a parent root and a nested canonical deliverable folder need skills, install skills separately in each repo. Each repo owns its own `.agents/skills/` folder and `.gitmodules`.

Do not install project-specific skills into a global agent skills folder unless the user explicitly asks for a global install.
