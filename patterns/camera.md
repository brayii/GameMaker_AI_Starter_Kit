# Camera

Use the simplest camera behavior that supports the current milestone.

## Options

- A simple follow camera keeps a target at a fixed or calculated point.
- A dead zone lets the target move within a region before the camera follows.
- Smoothing eases camera movement but can introduce lag or reveal room edges.
- Room bounds prevent the view from showing unintended space outside the playable area.

Document which object or system owns the camera and when it is created or destroyed. Prevent multiple owners from fighting over the same camera.

Keep camera and world-space logic separate from viewport placement and Draw GUI behavior. GUI elements should remain stable in screen space when the world camera moves.

## Testing

Test room edges, small rooms, target destruction or replacement, room transitions, teleports, fast movement, supported aspect ratios, viewport scaling, and GUI alignment. Final smoothing and framing require human testing in GameMaker.
