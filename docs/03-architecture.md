# Architecture

## Architecture goal

Keep the project easy to understand and easy to change.

## Main systems

| System | Responsibility | Main resources | Depends on |
|---|---|---|---|
| | | | |

## Ownership rules

State which object or system owns important data.

Examples:

- Race state is owned by `obj_race_controller`.
- Player input is read by `obj_car_player`.
- Lap progress is owned by each car or by the race controller.

## Communication

Describe how systems communicate:

- Direct instance references
- Parent object queries
- Functions
- Events
- Structs
- Global state
- Other

Use the simplest approach that fits the current project.

## Initialization order

Document required initialization relationships.

## Persistence

List persistent objects and explain why they persist.

## Global data

List every global variable and justify its use.

## Update flow

Describe the important per-step order.

## Draw flow

Describe world rendering and GUI rendering responsibilities.

## Technical constraints

- Target frame rate:
- Resolution strategy:
- Input requirements:
- Save requirements:
- Export targets:

## Deferred decisions

List architectural decisions intentionally postponed.
