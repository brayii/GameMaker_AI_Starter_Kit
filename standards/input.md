# Input

Define player actions before binding devices. Distinguish pressed, held, and released behavior so one-step actions do not repeat accidentally.

## Ownership

Use one clear owner for translating keyboard, mouse, and gamepad state into actions when several systems share input. Direct checks are acceptable for a small isolated behavior. Avoid duplicating raw input checks across many objects.

Separate gameplay input from menu input. Modal menus and pause must suppress or redirect gameplay actions deliberately. Add rebinding only when required by the project.

## Devices

- Normalize analog values only as needed and document dead zones.
- Handle gamepad connection, disconnection, and reassignment safely.
- Use the correct coordinate space for mouse input.
- Provide keyboard or other required alternatives according to the project accessibility goals.

## Testing

Test pressed, held, and released actions; simultaneous and conflicting inputs; keyboard, mouse, and each supported gamepad; analog thresholds; disconnect and reconnect; menu focus; pause suppression; and room transitions. Do not mandate a large input framework for a small game.
