# Development Workflow

Follow this workflow for every repository change. Prefer a small, reviewable change over a broad speculative one.

## Roles

- The human owner defines the gameplay goal, decides when behavior is good enough, approves commits, and authorizes pushes.
- The planning assistant clarifies behavior and scope, prepares implementation tasks, and performs independent reviews.
- Codex inspects the repository, implements approved work, validates it, reports results, and prepares changes for review.
- GameMaker is the authority for compilation, runtime behavior, asset setup, and gameplay feel.

## Default lifecycle

1. The human defines the gameplay goal.
2. The planning assistant clarifies behavior and scope.
3. Project documents and diagrams are updated.
4. Codex inspects the repository and current Git state.
5. Codex implements the smallest coherent change.
6. Codex reviews the complete diff and performs available validation.
7. Codex reports results and stops before committing.
8. An independent code review is performed.
9. The human approves the change or requests corrections.
10. Codex commits only after explicit approval.
11. Codex pushes only after separate explicit approval.

Never commit without explicit approval. Never push without explicit approval. Do not modify unrelated files.

## New features

- Confirm the current milestone is ready in `docs/00-project-readiness.md`.
- Define player-facing behavior, acceptance criteria, manual tests, and exclusions.
- Inspect related resources and extend the existing architecture.
- Update project documents or diagrams when the design changes.

## Bug fixes

- Record expected behavior, actual behavior, and reproduction steps.
- Identify the probable cause before editing.
- Repair the existing implementation before considering a rewrite.
- Retest the reproduction case and nearby behavior.

## Refactors

- Require a measurable correctness, maintenance, or performance problem.
- State which behavior must remain unchanged and which files are in scope.
- Validate behavior before and after the change.
- Do not introduce a framework without a demonstrated need.

## Documentation changes

- Check every changed reference and nearby authoritative document.
- Keep terminology and workflow gates consistent.
- Do not claim that code or runtime behavior changed.

## Milestone completion

- Confirm the acceptance criteria and manual test results.
- Review resource changes, documentation, diagrams, and the complete Git diff.
- Record remaining risks and follow-up work.
- Store an independent review under `reviews/` when appropriate.
- Wait for explicit commit approval, then wait for separate push approval.

## Completion gate

Before completing any task:

1. Review the complete Git diff.
2. Verify the implementation against `AGENTS.md` and the relevant standards.
3. Verify affected project documents and diagrams.
4. List assumptions and tests that were not run.
5. Stop and wait for independent review and approval before committing.
