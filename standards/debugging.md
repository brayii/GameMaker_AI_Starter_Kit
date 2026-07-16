# Debugging

Start with a reproducible report: expected behavior, actual behavior, steps, frequency, environment, and compiler or runtime messages.

## Diagnostics

- Add focused logging around the suspected path rather than logging every step globally.
- Use optional overlays to visualize state, collision bounds, paths, targets, timers, or ownership when that shortens diagnosis.
- Gate development-only diagnostics behind an existing debug setting or a clearly documented temporary flag.
- Preserve the original error context and avoid broad silent error suppression.
- Remove or disable temporary diagnostics after the cause is verified unless they provide lasting value.

Report the actual root cause when known, the evidence supporting it, and the smallest correction. If only a symptom was mitigated, say so. Never convert uncertainty into an unrelated defensive framework.
