# Enemy AI

Prefer small, explicit behavior built from the checks the enemy actually needs.

Useful building blocks include:

- A small finite state machine
- Timers and cooldowns
- Distance and angle checks
- Line-of-sight checks
- Collision and navigation checks
- Simple steering toward or away from a target

Give each state one clear responsibility and make transition conditions visible. Store state and timers on the enemy unless the architecture documents another owner. Handle missing or destroyed targets safely.

Avoid behavior trees, planners, or broad AI frameworks unless current requirements demonstrate a need.

## Debugging and testing

Provide temporary or optional visibility into the current state, target, timers, and transition reason when debugging requires it. Test detection boundaries, lost targets, blocked paths, cooldown completion, interruptions, room boundaries, multiple enemies, and recovery from invalid references. Human testing determines whether reactions are readable, fair, and enjoyable.
