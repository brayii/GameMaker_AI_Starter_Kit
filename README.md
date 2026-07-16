# GameMaker AI Starter Kit

A reusable documentation and workflow foundation for AI-assisted GameMaker development.

Copy this template into the root of a new blank GameMaker project or an existing GameMaker project. Create a blank project in GameMaker before using the template for a new game. This repository intentionally contains no generated `.yyp`, `.yy`, `.gml`, object, room, sprite, or other GameMaker resource files.

## Roles

- The human owner is the creative director and product owner. They decide what the game should be, test gameplay, approve commits, and authorize pushes.
- The planning assistant acts as technical lead. It clarifies systems, prepares Codex tasks, and performs independent reviews.
- Codex is the implementation engineer. It inspects the repository, makes scoped changes, performs self-review, and prepares work for approval.
- GameMaker builds, runs, and validates the game.

The human owner does not need to write GML. Codex can implement the documented game after onboarding and planning are complete. The human still compiles, runs, and evaluates the game in GameMaker.

## Workflow

```text
Design -> Codex implementation -> Codex self-review -> GameMaker test
       -> Independent review -> Human approval -> Commit -> Optional push
```

Codex never commits without explicit approval and never pushes without separate explicit approval. The full process is defined in `standards/development-workflow.md`.

## Start here

1. Create or open a GameMaker project and save it.
2. Copy this template into the directory containing its `.yyp` file.
3. Use `prompts/onboard-project.md` to inspect the project and populate `docs/00-project-inventory.md`.
4. Complete `docs/00-project-readiness.md` and the planning files in order.
5. Update relevant diagrams.
6. Give Codex a focused task with acceptance criteria and manual tests.
7. Test the result in GameMaker.
8. Review the complete Git diff independently.
9. Approve corrections or the commit.
10. Authorize a push separately when desired.

If there is no `.yyp` file, Codex must stop rather than fabricate a GameMaker project. If multiple `.yyp` files exist, the user must identify the target.

### New-project onboarding

Create and save a blank project in GameMaker first. Codex inspects that project's current format, records decided facts, marks unknowns, and establishes only what the first milestone requires.

### Existing-project onboarding

Codex inventories resources, architecture, ownership, rooms, persistence, data, conventions, protected systems, and technical debt before major implementation. Existing deliberate project choices take priority over template defaults.

## Template structure

```text
AGENTS.md                     Codex entry point and safety gates
README.md                     Template overview and onboarding
docs/                         Project-specific plans and milestones
diagrams/                     Project and workflow diagrams
standards/                    Authoritative reusable working standards
patterns/                     Optional, problem-specific design guidance
prompts/                      Reusable task and review prompts
reviews/                      Durable milestone and feature reviews
source-assets/                Editable source art and audio
tools/                        Optional project utilities
builds/                       Ignored local build output
gamemaker-project-layout.md   Expected copied-project layout
```

GameMaker creates and manages the actual project and resource folders in the target project; they are not included in this template repository.

## Documentation

Complete these project-specific files in order:

1. `docs/00-project-inventory.md`
2. `docs/00-project-readiness.md`
3. `docs/01-game-vision.md`
4. `docs/02-gameplay.md`
5. `docs/03-architecture.md`
6. `docs/04-object-plan.md`
7. `docs/05-room-plan.md`
8. `docs/06-asset-plan.md`
9. `docs/07-roadmap.md`
10. `docs/08-testing.md`

`docs/00-project-readiness.md` is the only authority for milestone implementation readiness.

## Standards, patterns, and reviews

- `standards/` defines onboarding, the development lifecycle, GameMaker project and resource safety, GML style, input, UI, audio, data, lifecycle, debugging, validation, and independent review.
- `patterns/` provides optional guidance for common systems such as input, HUDs, audio, pause, transitions, movement, cameras, saves, FSMs, and enemy AI. Use only relevant patterns after inspecting the current project.
- `reviews/` stores durable review decisions, findings, test results, follow-up tasks, and commit references.

The documentation guides implementation without replacing GameMaker compilation, runtime testing, visual inspection, or gameplay-feel evaluation. Build one playable milestone at a time.
