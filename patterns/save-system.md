# Save System

Add persistence only as the project requires it. Prefer this progression:

1. Variables for session-only state.
2. Structs for grouped runtime data.
3. JSON for durable, inspectable saves.
4. Advanced persistence only when requirements justify it.

## Durable saves

- Include a save-format version when saved data may evolve.
- Supply defaults for missing optional fields.
- Validate loaded types and required values before use.
- Migrate supported older versions deliberately.
- Use stable domain identifiers for durable records.
- Never save instance IDs as permanent identifiers.
- Write and replace save data using the safest approach supported by the project and target platform.

## Testing

Manually test creating a save, loading it after restart, overwriting it, missing fields, supported older versions, invalid or partial data, and target-platform paths. Confirm that load failures produce a recoverable result rather than corrupting current state.
