# Intent

Define the missing agent-skills component for the mini coding agent so it can discover reusable instruction packs, match them to user prompts, and run the appropriate skill at the right time.

## Goals

- Add a skill registry that scans the repository for reusable skill folders.
- Match skill instructions to user requests using a lightweight similarity check.
- Log requests, similarity scores, and the triggered skill for traceability.
- Keep the runtime simple, auditable, and compatible with the existing tool-driven agent loop.
