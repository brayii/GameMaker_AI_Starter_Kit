# Coding Standards

## General

- Use modern GML.
- Prefer clarity over cleverness.
- Keep functions and events focused.
- Initialize variables before use.
- Avoid unexplained magic numbers.
- Comment why important logic exists.
- Match existing project conventions.

## Naming

- Objects: `obj_name`
- Sprites: `spr_name`
- Sounds: `snd_name`
- Rooms: `rm_name`
- Fonts: `fnt_name`
- Shaders: `shd_name`

Use the project's existing conventions when they differ.

## State

Prefer instance-owned state.

Use globals only for truly global data and document them in `docs/03-architecture.md`.

## Functions

Prefer parameters and return values over hidden dependencies.

## Structs

Use structs for grouped data with a clear purpose.

## Events

Keep event code readable. Move reusable or complex logic into focused functions.

## Performance

Optimize only after identifying a real bottleneck.
