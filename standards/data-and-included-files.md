# Data and Included Files

Use JSON, CSV, localization, dialogue, and configuration files when external data makes the project easier to maintain. Included Files are shipped read-only project data; save data is user or session data written to an appropriate runtime location.

## Loading rules

- Follow the project's path and Included Files conventions.
- Account for platform-sensitive paths and file availability.
- Check that required files exist and report missing required data clearly.
- Provide documented defaults for optional fields or optional files.
- Validate parsed types, ranges, required keys, and record structure before use.
- Version data that must evolve compatibly.
- Keep localization keys and dialogue identifiers stable when saves or other data reference them.

Fail safely without broad silent suppression. Preserve enough context to identify the file and invalid field. Do not expose credentials or assume desktop filesystem behavior on every target platform.
