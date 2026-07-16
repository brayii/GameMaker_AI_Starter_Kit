# Expected GameMaker Project Layout

Copy this template into the directory containing a GameMaker-created `.yyp` file. A combined project will commonly contain both template guidance and GameMaker-managed resources.

```text
ProjectRoot/
|-- AGENTS.md
|-- README.md
|-- gamemaker-project-layout.md
|-- docs/
|-- standards/
|-- patterns/
|-- diagrams/
|-- prompts/
|-- reviews/
|-- source-assets/
|-- tools/
|-- builds/
|-- MyGame.yyp
|-- objects/
|-- scripts/
|-- rooms/
|-- sprites/
|-- sounds/
|-- fonts/
|-- shaders/
|-- paths/
|-- sequences/
|-- tilesets/
|-- timelines/
|-- extensions/
|-- options/
|-- datafiles/
`-- other GameMaker-managed resource folders
```

The template repository contains the guidance folders but no `.yyp` or GameMaker-generated resources. GameMaker must create and manage the exact resource structure for the installed version and selected assets.

Do not create empty resource folders or fake metadata merely to match this example.
