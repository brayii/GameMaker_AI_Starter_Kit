# GameMaker Codex Project Instructions

## Purpose

This reusable starter kit is copied into a new or existing GameMaker project for AI-assisted development.

The human owner defines the game, tests gameplay, approves commits, and authorizes pushes. The planning assistant clarifies designs and performs independent reviews. Codex inspects and edits the repository. GameMaker is the final authority for compilation, runtime behavior, asset setup, and gameplay feel.

## Priorities

1. Correctness
2. Playable results
3. Simplicity
4. Readability
5. Maintainability
6. Performance only after a real problem is identified

Avoid unnecessary architecture. A small working system is preferable to a large speculative framework.

## Authority

Use this order when making decisions:

1. Current project code and resource structure
2. Explicit current task requirements
3. Detailed project decisions under `docs/`
4. This `AGENTS.md`
5. Files under `standards/`
6. Files under `diagrams/`
7. Relevant files under `patterns/`
8. Current official GameMaker documentation for engine behavior

Current official GameMaker documentation is authoritative for engine syntax and behavior. Project code, current task requirements, and detailed project documents control project-specific design decisions.

Never invent GameMaker functions, events, APIs, metadata fields, or engine behavior.

## Required reading

Always read:

1. `AGENTS.md`
2. `standards/development-workflow.md`
3. `docs/00-project-readiness.md`
4. `docs/01-game-vision.md`
5. `docs/07-roadmap.md`

Then read the standards, project documents, diagrams, and patterns relevant to the task.

- Read `standards/gamemaker-projects.md` and `standards/project-onboarding.md` when onboarding a project or before initial major implementation.
- Read `standards/resources-and-assets.md` for visual, audio, data, extension, and other asset resources.
- Read `standards/input.md`, `standards/ui-and-gui.md`, `standards/audio.md`, `standards/data-and-included-files.md`, `standards/debugging.md`, and `standards/lifecycle-and-pause.md` when those systems are affected.
- Read `docs/00-project-inventory.md` before major implementation in an existing project.
- Read relevant files under `patterns/` only when the task matches them. Patterns are optional guidance, not mandatory architecture.

Then inspect the current GameMaker project and existing code.

## Workflow and planning gates

Follow `standards/development-workflow.md` for every task.

Do not begin GameMaker resource or gameplay implementation until:

- Exactly one target `.yyp` project has been identified according to `standards/gamemaker-projects.md`.
- Project onboarding and `docs/00-project-inventory.md` are complete enough for the current work.
- The current milestone is marked ready in `docs/00-project-readiness.md`.

If no `.yyp` file exists, do not fabricate a GameMaker project. Tell the user to create and save a blank project in GameMaker first, then stop before GameMaker implementation. Documentation-only maintenance of this reusable template does not require a `.yyp` file. If multiple `.yyp` files exist, report them and ask which project is in scope.

If the project foundation or current milestone is incomplete, report the missing items instead of inventing requirements.

## Essential project safety

Before editing:

1. Review Git status.
2. Locate the target `.yyp` file.
3. Inspect relevant existing objects, scripts, rooms, assets, and resources.
4. Find similar resources and follow their format and conventions.
5. Determine the smallest coherent change.

GameMaker resources may require coordinated edits to the `.yyp`, resource `.yy` files, event `.gml` files, room metadata, instance creation code, resource ordering, and folder metadata.

- Preserve unknown metadata fields and never duplicate identifiers.
- Improve before replacing and extend before rewriting.
- Do not create empty events or speculative resources.
- Do not rename, move, or delete assets unless explicitly requested.
- Do not modify generated, cache, build, or temporary directories.
- Keep metadata edits minimal and review the complete diff.
- Recommend that GameMaker be saved and closed before structural project-file edits.
- Do not fabricate finished artwork or audio unless assets are provided.

## Editing boundaries

Unless explicitly requested, do not:

- Reorganize the project or rewrite working systems
- Change room order or the starting room
- Modify export settings or credentials
- Replace artwork or audio
- Add external dependencies
- Commit, push, or publish changes

Never commit without explicit approval. Never push without separate explicit approval.

## Validation and completion

Follow `standards/testing-and-validation.md`. Never claim compilation, runtime testing, or manual testing unless it actually occurred.

Before completing a task:

1. Review the complete Git diff.
2. Verify the implementation against this file and relevant standards.
3. Verify affected documentation and diagrams.
4. Check resource references, identifiers, initialization, parent behavior, and room instances as applicable.
5. List assumptions, unavailable tests, manual setup, and risks.
6. Stop and wait for independent review before committing.

## Required completion report

### Summary

Describe the implemented behavior.

### Files changed

List every created, modified, renamed, or deleted file.

### GameMaker resources changed

List every affected object, event, script, room, sprite, sound, shader, and other resource.

### Validation performed

State exactly what was inspected or executed.

### Manual GameMaker test

Provide numbered test steps.

### Remaining manual setup

List editor work, art, audio, masks, origins, room placement, camera setup, or export work.

### Risks and assumptions

State anything that could not be verified.

## Project-specific values

This section is a concise summary. Detailed values belong in the relevant project documents under `docs/`. If a summary value conflicts with a detailed project document, the detailed project document is authoritative.

Complete these before implementation:

- Project name:
- GameMaker version:
- Genre:
- Main player object:
- Main controller object:
- Parent enemy object:
- Starting room:
- Main gameplay room:
- Movement model:
- Collision model:
- Camera model:
- Save format:
- Target platforms:
- Build command:
- Systems that must not be modified:
