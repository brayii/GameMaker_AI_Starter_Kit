# Audio

Use direct playback when it is sufficient. Introduce centralized audio ownership only when music continuity, categories, transitions, or shared state require it.

## Playback and ownership

- Give music playback one clear owner and prevent duplicate tracks after room changes.
- Define which sounds loop and how each loop stops.
- Keep sound-effect, music, and other required volume categories consistent.
- Use fades and transitions only when they support the intended experience.
- Document whether pause stops, pauses, ducks, or leaves each audio category unchanged.
- Preserve intended music behavior across room transitions.

Store and validate audio handles only when later control is required. Stop or release owned playback during cleanup when appropriate. Handle missing optional resources safely; report missing required resources instead of silently hiding the problem.

Human testing is required for balance, clipping, repetition, loop seams, fades, pause behavior, transition timing, and target-platform output.
