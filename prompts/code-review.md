# GameMaker Code Review Request

Review the supplied Git diff and changed files against:

- `AGENTS.md`
- Project documentation
- Project diagrams
- Existing GameMaker architecture

Focus on:

1. Invalid or undocumented GML
2. Incorrect event placement
3. Initialization-order problems
4. Parent event mistakes
5. Invalid asset or instance references
6. Room and metadata inconsistencies
7. Collision and timing bugs
8. Frame-rate dependence
9. Save compatibility
10. Unnecessary architecture
11. Unrelated changes
12. Missing test coverage

Report findings by severity:

- Critical
- High
- Medium
- Low

For each finding include:

- File and location
- Problem
- Why it matters
- Smallest recommended correction

Finish with a focused Codex correction task.
