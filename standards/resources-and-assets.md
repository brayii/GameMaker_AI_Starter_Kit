# Resources and Assets

These rules apply to sprites, sounds, fonts, tile sets, shaders, sequences, paths, animation curves, particle systems, Included Files, and extensions.

## Before editing

1. Confirm the resource is required by the current milestone.
2. Inspect a similar current-project resource and its references.
3. Follow established names, folders, groups, and metadata format.
4. Coordinate every required project, folder, room, object, script, and resource reference.

Preserve unknown metadata fields and use unique identifiers. Never invent unsupported fields or copy identifiers from another resource. Stop when the current project provides no safe example and recommend editor creation when GameMaker should generate the structure.

## Asset boundaries

- Do not fabricate finished art or audio unless explicitly requested and supported by provided assets.
- Preserve editable sources under `source-assets/` and imported resources in GameMaker-managed folders.
- Report editor-only setup and configuration clearly.
- Do not add an extension without explicit approval and a demonstrated need.
- Treat Included Files as shipped project data, not save data.

Human validation is required for sprite origins, collision masks, animation timing, font coverage, tile alignment, sequence timing, paths, visual layout, shader output, particle effects, audio balance, and platform-specific extension behavior.
