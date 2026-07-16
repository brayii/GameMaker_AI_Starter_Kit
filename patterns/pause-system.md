# Pause System

## When useful

Use a coordinated pause system when several gameplay, input, animation, timer, UI, or audio systems must pause consistently.

## When unnecessary

Skip it when the game has no pause requirement or one isolated behavior can stop locally.

## Ownership and responsibilities

One documented owner controls pause state. Each affected system follows a documented pause policy instead of assuming all GameMaker activity stops automatically. The pause UI owns only presentation and navigation unless the architecture assigns it pause state.

## Common failures

- Gameplay input leaks through the pause menu.
- Alarms, timers, animation, or audio continue unexpectedly.
- Multiple pause menus or owners appear.
- Unpause resets state it did not own.
- Room changes leave the game paused unintentionally.

## Testing checklist

- Pause during movement, alarms, animation, audio, and transitions.
- Test menu navigation and input suppression.
- Test room restart, return to menu, and game restart.
- Confirm cleanup and state restoration.
