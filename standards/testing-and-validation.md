# Testing and Validation

Codex validates source, structure, references, and Git changes where tools permit. The human owner validates the project in GameMaker.

## Codex responsibilities

- Review the complete Git diff and confirm there are no unrelated changes.
- Check GML syntax as far as available tools allow.
- Verify changed resource, asset, event, room, folder, and project references.
- Check for duplicate resource and room-instance identifiers.
- Review initialization order and parent-event behavior.
- Check persistent controllers and room-instance placement.
- Review save changes for version and compatibility risks.
- Check input, collision, movement, cooldown, and animation logic for timing assumptions.
- Update affected documentation and diagrams.
- Run configured validation or build commands when available.

## Human GameMaker responsibilities

- Open and compile the project.
- Check compiler messages and runtime errors.
- Test the main behavior, edge cases, and existing related behavior.
- Test keyboard, mouse, and gamepad input that is in scope.
- Test collisions, room transitions, cameras, persistence, and save loading as applicable.
- Check behavior at supported frame rates and resolution settings.
- Perform visual, audio, gameplay-feel, and export validation.

## Reporting

Report exactly what was inspected or executed. Never claim that GameMaker compiled, that runtime behavior passed, or that a manual test was performed unless it actually occurred.

Provide numbered manual test steps with expected results. Record failed or unrun steps, remaining editor work, assumptions, and risks. If save data changed, include tests for new saves, existing supported saves, missing fields, and invalid data where applicable.
