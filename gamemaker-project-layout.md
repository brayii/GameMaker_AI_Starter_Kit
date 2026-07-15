# Expected GameMaker Project Layout

After creating a GameMaker project in this repository, the root will commonly contain a `.yyp` file and GameMaker-managed resource folders.

Example:

```text
ProjectRoot/
├── AGENTS.md
├── README.md
├── MyGame.yyp
├── docs/
├── diagrams/
├── prompts/
├── source-assets/
├── tools/
├── builds/
├── objects/
├── scripts/
├── rooms/
├── sprites/
├── sounds/
├── fonts/
├── shaders/
├── paths/
├── sequences/
├── tilesets/
├── timelines/
├── extensions/
├── options/
├── datafiles/
└── other GameMaker-managed resource folders
```

GameMaker should create and manage the exact resource structure for the installed version and selected assets.

Do not create empty fake resource metadata merely to match this diagram.
