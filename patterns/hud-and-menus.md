# HUD and Menus

## When useful

Use a shared UI owner when HUD elements, menus, focus, and modal screens share state or must persist consistently.

## When unnecessary

Skip it for one isolated label or prompt.

## Ownership and responsibilities

Document who owns displayed data, navigation focus, modal priority, and transitions. Draw GUI-space elements using the project's scaling and anchoring rules. Keep UI presentation separate from gameplay ownership where practical.

## Common failures

- Duplicate persistent UI controllers
- Incorrect mouse coordinate space
- Lost or invisible focus
- Gameplay input leaking through modal screens
- Layout breaking at other aspect ratios
- UI state surviving or resetting unintentionally between rooms

## Testing checklist

- Test supported resolutions and aspect ratios.
- Test mouse, keyboard, and gamepad navigation.
- Test focus recovery, modal priority, pause, and room transitions.
- Verify readable feedback and correct anchors.
