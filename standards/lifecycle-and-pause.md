# Lifecycle and Pause

Document ownership and state changes across game start, Room Start, Room End, room restart, return to menu, and full game restart.

## Lifecycle

- Create persistent objects once and prevent duplicate controllers after transitions or restarts.
- Decide which state survives room changes, return to menu, and game restart.
- Release owned data structures, surfaces, buffers, handles, and temporary references at the correct lifecycle point.
- Reacquire or validate references that may become invalid after a room change.
- Keep Room Start and Room End behavior focused on transition-specific work.

## Pause

Give pause state one clear owner. Define which input remains active, how gameplay input is suppressed, and whether alarms, timers, movement, animation, particles, audio, and asynchronous results continue, freeze, or are handled specially.

Pause must not create duplicate menus or controllers. Unpausing should restore only the state pause changed. Test pausing during transitions, alarms, animation, audio, controller disconnection, room restart, return to menu, and game restart.
