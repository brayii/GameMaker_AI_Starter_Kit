# GML Style

Prefer clear, modern GML that a beginner can follow and an experienced developer can maintain. Existing project conventions take priority when they are consistent and documented.

## Formatting

- Use four spaces for indentation.
- Use braces consistently for multiline blocks and wherever omission could reduce clarity.
- Keep functions and events focused.
- Comment why important logic exists, not what an obvious line does.
- Replace unexplained magic numbers with named variables, macros, or configuration data.

## Naming

- Instance and local variables: clear `snake_case` names.
- Function arguments: descriptive `snake_case` names.
- Macros: clear uppercase names when the project uses that convention.
- Enum types and members: follow one consistent project convention and avoid ambiguous abbreviations.
- Constructor functions: clear names that distinguish the created data type.
- Assets: follow project conventions; otherwise use prefixes such as `obj_`, `spr_`, `snd_`, `rm_`, `fnt_`, and `shd_`.

## Language features and state

Prefer modern functions, methods, structs, arrays, and enums. Initialize variables explicitly before use. Prefer instance-owned state and parameters or return values over hidden dependencies. Use globals only for truly global data and document them in `docs/03-architecture.md`.

Use arrays for simple ordered collections and fixed or moderately sized data. Use DS structures only when their specific behavior is needed or the existing project already relies on them. Destroy owned DS structures and release other runtime resources in the appropriate cleanup path.

## Defensive behavior

Validate references and external data at boundaries where failure is plausible. Provide safe defaults for optional data. Do not bury design or initialization errors under broad defensive checks.

## Timing and performance

Follow the project's documented room-speed or delta-time model. Do not mix timing models without a clear reason. Review movement, alarms, cooldowns, animation, and collision behavior for frame-rate assumptions.

Optimize only after identifying a real bottleneck. Prefer a small readable implementation until measurement shows that complexity is justified.
