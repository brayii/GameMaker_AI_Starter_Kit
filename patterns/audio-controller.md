# Audio Controller

## When useful

Use shared audio ownership when music persists across rooms, volume categories are global, or fades and transitions need coordination.

## When unnecessary

Skip it for a few independent sound effects.

## Ownership and responsibilities

The owner prevents duplicate music, applies category volumes, coordinates transitions, and tracks only handles that require later control. Gameplay objects may still request local sound effects directly when that remains clear.

## Common failures

- Music restarts or layers after room changes.
- Loop handles are lost and cannot be stopped.
- Pause and volume changes affect the wrong sounds.
- Persistent audio owners are duplicated.
- Missing resources fail silently.

## Testing checklist

- Test repeated room transitions and restarts.
- Test pause, unpause, volume categories, fades, and loop cleanup.
- Test missing optional and required resources.
- Check balance and transitions in GameMaker.
