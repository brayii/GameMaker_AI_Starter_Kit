# UI and GUI

Give the HUD, menus, and modal screens clear ownership. Reuse an existing UI owner when practical and prevent duplicate persistent UI controllers.

## Layout and interaction

- Draw screen-space interface in Draw GUI unless the project deliberately uses another model.
- Follow the documented GUI resolution and scaling strategy.
- Anchor elements to intended edges, centers, or safe areas rather than one test resolution.
- Convert or read mouse coordinates in the correct GUI space.
- Make focus, selection, confirmation, cancellation, and modal priority explicit.
- Ensure pause menus suppress gameplay input according to the pause design.
- Preserve UI state deliberately across room transitions.

Provide more than color alone for important feedback when practical. Keep text readable, selection visible, and critical actions understandable.

## Testing

Test supported aspect ratios and resolutions, GUI scaling, anchors, mouse hit areas, keyboard and gamepad navigation, focus recovery, modal stacking, pause behavior, room transitions, and duplicate-controller prevention. Final visual layout and accessibility feedback require human testing.
