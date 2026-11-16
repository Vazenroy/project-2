# Specification

## Functional requirements

1. The agent must discover skill folders under the repository root.
2. Each skill folder must contain a `skill.md` file with actionable instructions.
3. The agent must compare the incoming prompt to discovered skills using a similarity check.
4. When a match is strong enough, the agent injects the matching instructions into the execution flow.
5. The agent must persist a session log of:
   - the original prompt,
   - the computed similarity score,
   - the selected skill name and path.
6. The implementation must not break the existing tool contract or session resume flow.

## Non-functional requirements

- The skill system must be lightweight and deterministic.
- Matching should rely on token overlap and keyword scoring rather than external dependencies.
- Logs should remain small and readable.
- Skills should be discoverable in normal repo layouts without requiring custom runtime registration.
