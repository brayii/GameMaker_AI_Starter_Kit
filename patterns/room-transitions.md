# Room Transitions

## When useful

Use coordinated room transitions when fades, loading, persistent state, or destination setup must occur in a controlled order.

## When unnecessary

Use a direct room change when no coordination is needed.

## Ownership and responsibilities

Give transition state one clear owner. It validates the destination, prevents duplicate requests, coordinates optional visual or audio effects, changes rooms once, and releases transition state afterward.

## Common failures

- Multiple requests trigger competing room changes.
- Persistent controllers duplicate in the destination.
- Input remains active during a blocking transition.
- References survive after their instances are destroyed.
- Fade, music, or loading state never completes.

## Testing checklist

- Test every permitted source and destination.
- Test repeated and simultaneous requests.
- Test persistent objects, input suppression, cameras, UI, and audio.
- Test invalid destinations, room restart, and return to menu.
