# Objects and Events

Inspect similar objects and the current project format before creating or editing an object.

## Creating objects

1. Confirm an existing object or focused function cannot satisfy the requirement.
2. Follow established naming, folder, metadata, and parent conventions.
3. Choose a parent only when behavior or classification is genuinely shared.
4. Assign a sprite or collision mask only when specified by the design or supported by existing resources.
5. Add only required events and create their matching event GML files.
6. Register all required project and folder references.
7. Verify parent, sprite, mask, script, and room references.

Do not add empty events. Do not add a Draw event when default drawing is sufficient.

## Event responsibilities

- Create: initialize instance-owned state and acquire required references.
- Step: regular gameplay updates.
- Begin Step: work that must occur before normal Step processing.
- End Step: work that depends on completed Step behavior.
- Draw: custom world rendering.
- Draw GUI: screen-space interface rendering.
- Alarm: focused delayed or scheduled behavior.
- Collision: collision responses that fit the project's collision model.
- Clean Up: release data structures, surfaces, buffers, and other owned resources.
- Destroy: destruction behavior that must occur specifically when the instance is destroyed.
- Room Start and Room End: behavior tied to room transitions.
- Async: only the documented callback for the asynchronous system involved.

Keep each event focused. Move reusable or complex logic into a function when that makes the event clearer.

## Inheritance

Inspect the parent object's event before changing a child event. Use `event_inherited()` only when the parent implementation should also run and the execution order is understood. Do not call it automatically, and do not silently discard required parent behavior.

## Initialization and references

Initialize instance variables before use. Document important initialization order and handle references that can become invalid. Confirm an event does not already exist before adding it, preserve unknown metadata fields, and verify that event metadata matches its GML file before finishing.
