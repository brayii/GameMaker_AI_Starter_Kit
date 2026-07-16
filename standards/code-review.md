# Code Review

Independent review occurs after Codex self-review and before commit approval. Review the complete diff, changed files, relevant project documents, diagrams, standards, and current GameMaker architecture.

## Severity

- Critical: corrupts the project or data, prevents compilation or core use, or creates a severe security or release risk.
- High: likely runtime failure, major incorrect behavior, or unsafe resource structure.
- Medium: meaningful correctness, maintenance, compatibility, or testing problem.
- Low: limited issue that is worth correcting but does not threaten the feature.

## Review areas

- Invalid or undocumented GML
- Incorrect event placement
- Initialization-order bugs
- Parent-event mistakes
- Invalid asset or resource references
- Room metadata and instance issues
- Collision, timing, and frame-rate bugs
- Save compatibility
- Unnecessary architecture
- Unrelated changes
- Missing manual tests
- Documentation drift

## Finding format

Each finding must include:

- File and location
- Problem
- Why it matters
- Smallest recommended correction

Do not inflate severity or report speculative style preferences as defects. If there are no findings, say so and identify any testing limitations.

Finish with either a focused Codex correction task or explicit approval to commit. Commit approval does not authorize a push.
