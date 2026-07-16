# GameMaker Projects

Use these rules after this template has been copied into a new or existing GameMaker project. This template does not generate a GameMaker project from an empty folder.

## Locate the project

Search the repository for `.yyp` files before GameMaker resource or gameplay implementation.

- If none exist, do not fabricate a project or metadata. Ask the user to create a blank project in GameMaker, save it, and copy this template into its root. Stop before GameMaker implementation. Documentation-only maintenance of the reusable template may continue.
- If exactly one exists, treat its directory as the GameMaker project root.
- If more than one exists, list them and ask the user which project is in scope. Do not guess.

## Inspect before editing

1. Review Git status and confirm unexpected changes are understood.
2. Inspect the `.yyp` file and GameMaker-managed folders.
3. Identify the resource format, naming, folder, ordering, and reference conventions already present.
4. Inspect relevant objects, scripts, rooms, assets, options, and resource files.
5. Find the closest similar resource before creating or changing one.
6. Determine the smallest coordinated change.

For a new blank project, learn its format from the files GameMaker created. For an existing project, preserve its established architecture and conventions.

## Metadata safety

- Never invent GameMaker APIs, event identifiers, metadata fields, or resource formats.
- Preserve unknown `.yy` and `.yyp` fields.
- Keep structural edits minimal and coordinated across project, resource, event, room-order, and folder references.
- Never copy identifiers from another resource. Check all new resource and room-instance identifiers for uniqueness.
- Do not rename, move, or delete resources unless explicitly requested.
- Recommend saving and closing GameMaker before structural project-file edits.
- Do not edit generated, cache, build, or temporary output.

## Editor boundaries

Use repository edits when the current project provides a clear, verifiable format and all required references can be updated safely. Recommend manual GameMaker editor work when the format is uncertain, the change depends on editor-generated data, or visual configuration must be judged in the editor.

Art, audio, collision masks, sprite origins, animation settings, cameras, and gameplay feel require final human validation in GameMaker.

## Stop conditions

Stop and report uncertainty when:

- The target project is ambiguous.
- No real GameMaker project exists.
- A required metadata format has no current-project example.
- Existing references or identifiers appear inconsistent.
- A requested change would require guessing engine behavior.
- User input is required to choose among materially different project structures.

Do not turn uncertainty into invented metadata.
