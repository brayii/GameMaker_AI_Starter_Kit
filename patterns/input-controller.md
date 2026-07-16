# Input Controller

## When useful

Use a shared input owner when multiple objects need consistent actions, device switching, analog processing, rebinding, or menu/gameplay routing.

## When unnecessary

Skip it when one small object can read a few inputs clearly.

## Ownership and responsibilities

One documented owner translates raw device state into pressed, held, released, and analog actions. It tracks active devices only when needed and exposes actions without owning unrelated gameplay decisions.

## Common failures

- Duplicate raw checks produce inconsistent behavior.
- Pressed actions are treated as held.
- Dead zones differ between consumers.
- Gameplay input remains active under menus or pause.
- Disconnected devices leave stale state.

## Testing checklist

- Test every supported device and action phase.
- Test analog dead zones and simultaneous inputs.
- Disconnect and reconnect gamepads.
- Move between gameplay, menus, and pause.
- Confirm only one input owner exists when centralized ownership is used.
