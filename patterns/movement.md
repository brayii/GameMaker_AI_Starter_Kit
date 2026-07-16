# Movement

Choose movement based on the intended feel and the project's existing collision and timing models. There is no universal movement system.

## Approaches

- Direct movement applies the requested displacement immediately and suits precise or grid-like control.
- Acceleration and friction create momentum and require tuning for responsiveness, stopping distance, and direction changes.
- Subpixel movement stores precise position or remainder values while resolving collisions at the precision required by the project.
- Collision-aware movement separates intended movement from collision resolution and handles each axis or path according to the established collision model.

Do not mix built-in speed variables, manual position changes, physics, and custom collision without a documented reason.

## Timing and tuning

Follow the project's room-speed or delta-time assumption consistently. Record tuning values such as speed, acceleration, friction, gravity, and jump strength in the gameplay specification or clear configuration data. Avoid compensating twice for delta time.

## Testing

Test starting, stopping, reversing, diagonal input, boundaries, corners, tunneling, slopes or moving platforms when applicable, and behavior at supported frame rates. The human owner must judge responsiveness and gameplay feel in GameMaker.
