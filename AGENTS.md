# GameMaker Codex Project Instructions

## Purpose

This repository contains a GameMaker project developed with an AI-assisted workflow.

The human owner defines the game and tests gameplay.
The GameMaker planning assistant helps design features and review changes.
Codex inspects and edits the repository.
GameMaker is the final authority for compilation, runtime behavior, asset setup, and gameplay feel.

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
2. This `AGENTS.md`
3. Files under `docs/`
4. Files under `diagrams/`
5. Current official GameMaker documentation

Never invent GameMaker functions, events, APIs, metadata fields, or engine behavior.

## Required reading order

Before implementing a feature, read:

1. `AGENTS.md`
2. `docs/00-project-readiness.md`
3. `docs/01-game-vision.md`
4. `docs/02-gameplay.md`
5. `docs/03-architecture.md`
6. `docs/04-object-plan.md`
7. `docs/05-room-plan.md`
8. `docs/06-asset-plan.md`
9. `docs/07-roadmap.md`
10. `docs/08-testing.md`
11. `docs/09-coding-standards.md`
12. Relevant files under `diagrams/`

Then inspect the current GameMaker project and existing code.

## Planning gate

Do not begin implementation until the current milestone is marked ready in `docs/00-project-readiness.md`.

If the project foundation is incomplete, report the missing items instead of inventing requirements.

## Before editing

1. Locate the `.yyp` file.
2. Review `git status`.
3. Inspect relevant existing objects, scripts, rooms, and resources.
4. Find similar existing resources and follow their structure.
5. Identify naming, folder, parent-object, and event conventions.
6. Determine the smallest coherent change.
7. Avoid unrelated modifications.

Improve before replacing. Extend before rewriting.

## Project safety

GameMaker resources may require coordinated edits to:

- The main `.yyp` file
- Resource `.yy` files
- Event `.gml` files
- Room metadata
- Instance creation code
- Resource ordering and folder metadata

When creating or editing resources:

- Follow the format already used by this project.
- Preserve required identifiers and references.
- Never duplicate resource identifiers.
- Do not remove unknown metadata fields.
- Do not rename or move assets unless explicitly requested.
- Do not modify generated, cache, build, or temporary directories.
- Keep metadata edits minimal.
- Review the complete diff before finishing.

When structural project files will be changed, recommend that GameMaker be saved and closed first.

## Naming conventions

Use the project's existing conventions. When the project has no established convention, prefer:

- Objects: `obj_name`
- Sprites: `spr_name`
- Sounds: `snd_name`
- Rooms: `rm_name`
- Fonts: `fnt_name`
- Shaders: `shd_name`
- Tile sets: `ts_name`
- Sequences: `seq_name`
- Paths: `pth_name`

Use clear names over clever names.

## Creating objects

When creating an object:

1. Inspect similar objects.
2. Follow their resource and folder structure.
3. Decide whether a parent object should be used.
4. Assign a sprite only when specified or supported by the existing design.
5. Add only required events.
6. Create matching event GML files.
7. Register all required resource references.
8. Verify parent, sprite, mask, script, and room references.
9. Do not add empty events.
10. Do not add a Draw event when default drawing is sufficient.

## Event responsibilities

- Create: initialize instance-owned state.
- Step: gameplay logic that updates every game step.
- Begin Step: logic required before normal Step processing.
- End Step: logic dependent on completed Step behavior.
- Draw: custom world rendering.
- Draw GUI: screen-space interface rendering.
- Clean Up: release resources owned by the instance.
- Destroy: destruction behavior when specifically required.
- Alarm: delayed or scheduled instance behavior.
- Collision: use only when it fits the existing collision architecture.
- Room Start/End: room transition behavior.
- Async events: only for the documented asynchronous system involved.

Initialize variables before use. Check parent event behavior.

## Adding events

When adding an event to an existing object:

1. Confirm the event does not already exist.
2. Inspect how similar events are represented.
3. Add the event metadata.
4. Create the matching `.gml` file.
5. Preserve inherited behavior where required.
6. Keep the event focused.

If editing an existing event is sufficient, do not create another system.

## Scripts and functions

Prefer modern GML:

- Functions
- Methods
- Structs
- Arrays
- Enums
- Explicit initialization
- Clear parameters and return values

Keep functions focused. Avoid hidden dependencies and unnecessary global state.

Do not create a manager object merely to hold helper functions.

## Creating rooms

When creating a room:

1. Inspect similar rooms.
2. Match the current room metadata format.
3. Create only required layers.
4. Follow existing layer names and depth conventions.
5. Add only required instances.
6. Give every room instance a valid unique identifier.
7. Verify object references.
8. Add the room to required project and room-order references.
9. Do not change the starting room unless explicitly requested.
10. Preserve camera, viewport, dimensions, and persistence conventions.

## Room instances

Before placing an instance:

- Confirm the object exists.
- Check whether it is created dynamically elsewhere.
- Check whether a persistent controller already exists.
- Follow the room's current instance-layer structure.
- Set position and required properties explicitly.
- Add creation code only when needed.

## Visual and audio resources

Codex may create or edit metadata and supporting code, but final visual and audio validation belongs in GameMaker.

Do not fabricate finished artwork or audio unless assets are provided.

Preserve:

- Sprite dimensions
- Origins
- Collision masks
- Animation speed
- Texture groups
- Sound settings
- Font ranges
- Shader files and references

Report manual editor work clearly.

## Movement and collision

Before changing movement:

1. Inspect the current movement model.
2. Identify whether it uses built-in speed variables, manual movement, physics, or custom collision.
3. Preserve the current model unless it is fundamentally broken.
4. Avoid mixing movement systems without a clear reason.

Review:

- Subpixel movement
- Collision resolution
- Tunneling
- Slopes
- Moving platforms
- Room boundaries
- Frame-rate dependence
- Delta-time assumptions
- Collision masks

Gameplay feel must be tested by the human owner.

## AI

Prefer:

- Explicit finite state machines
- Timers
- Cooldowns
- Distance checks
- Angle checks
- Line-of-sight checks
- Collision checks
- Simple steering behavior

Use one clear responsibility per state.

Do not introduce behavior trees, planners, or broad AI frameworks without a demonstrated need.

## Save systems

Prefer this progression:

1. Variables
2. Structs
3. JSON serialization
4. More advanced persistence only when required

Do not store instance IDs as permanent save identifiers.

## Editing boundaries

Unless explicitly requested, do not:

- Rename or delete assets
- Reorganize the project
- Rewrite working systems
- Change room order
- Change the starting room
- Modify export settings or credentials
- Replace artwork or audio
- Add external dependencies
- Commit, push, or publish changes

## Validation

After implementation:

1. Review the complete Git diff.
2. Check every created and changed resource reference.
3. Check for duplicate identifiers.
4. Check GML syntax.
5. Check initialization order.
6. Check parent event behavior.
7. Check room instance references.
8. Check for unrelated metadata changes.
9. Run configured validation or build commands when available.
10. Never claim compilation or runtime testing unless it actually occurred.

## Required completion report

### Summary
Describe the implemented behavior.

### Files changed
List every created, modified, renamed, or deleted file.

### GameMaker resources changed
List every object, event, script, room, sprite, sound, shader, and other affected resource.

### Validation performed
State exactly what was inspected or executed.

### Manual GameMaker test
Provide numbered test steps.

### Remaining manual setup
List editor work, art, audio, masks, origins, room placement, camera setup, or export work.

### Risks and assumptions
State anything that could not be verified.

## Feature workflow

For each feature:

1. Read the project documents.
2. Restate the gameplay goal.
3. Inspect the existing implementation.
4. Propose the smallest implementation.
5. Implement it.
6. Review the diff.
7. Validate what can be validated.
8. Produce the required completion report.

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
