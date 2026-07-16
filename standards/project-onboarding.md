# Project Onboarding

Complete `docs/00-project-inventory.md` before major implementation. Follow `standards/gamemaker-projects.md` when locating the project and inspecting metadata.

## New projects

1. Confirm GameMaker created and saved exactly one blank `.yyp` project.
2. Inspect its current resource format instead of relying on a remembered format.
3. Record known facts in the project inventory and mark unresolved items clearly.
4. Complete the minimum planning gate for the first milestone.
5. Establish only the conventions and resources needed for that milestone.

Do not create speculative controllers, systems, rooms, or assets.

## Existing projects

1. Review Git status and identify the target `.yyp`.
2. Inventory resources, architecture, ownership, rooms, persistence, data, and conventions before changing architecture.
3. Preserve established behavior and deliberate project choices.
4. Document inconsistencies, protected systems, technical debt, and unknowns without silently normalizing them.
5. Apply template defaults only when the project has no established decision.

## File Watcher safety

- Save and close GameMaker before structural external edits when practical.
- Reopen the project after Codex finishes.
- Review changes detected by GameMaker's File Watcher.
- Reload disk changes instead of overwriting them with stale editor state.
- Compile immediately after reloading, then report any errors against the changed files.

If GameMaker and disk state appear to conflict, stop and preserve both until the human chooses the authoritative version.
