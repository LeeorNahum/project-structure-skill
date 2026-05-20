# AGENTS.md

This repo defines a project-structure skill. Keep it concise, evidence-driven, and free of context leaks.

## Editing Protocol

- Ask before touching each file.
- After editing a file, stop and ask for review before moving to the next file.
- Do not encode a structure rule as a default unless it is backed by observed project usage or an explicit preference.
- Clearly separate observed patterns from proposed patterns.
- Prefer removing questionable content over adding caveats around it.

## File Roles

- `SKILL.md`: trigger, core philosophy, verdict format, shape list, and instructions for when to load supporting files.
- `references/`: conditional guidance, decision rules, evidence notes, and non-copyable explanation.
- `assets/`: copyable templates or static resources that may be filled in or trimmed for a real project.
- `README.md`: short human-facing summary only.

If the same rule appears in multiple places, choose one owner and point to it from the others.

## Context Discipline

- Do not include personal names, chat history, temporary task context, or source-specific proper nouns in generic guidance.
- Do not copy details from one project into the skill unless they are being used as clearly labeled evidence.
- Do not mention external skills, sources, tools, or standards unless the file explains exactly why the agent needs them.
- Examples should use placeholders unless a section is explicitly documenting evidence from a real project.

## Before Finishing

- Confirm `SKILL.md` tells agents exactly when to read each reference or use each asset.
- Remove generic advice an agent already knows.
- Check for context leaks and unnecessary proper nouns.
- Update `metadata.version` when behavior changes.
