# Plan

## Phase 1: Skill discovery

- Search the repository for `skill.md` files.
- Treat each discovered file as a reusable skill pack.
- Collect the skill name from its parent directory.

## Phase 2: Prompt matching

- Normalize the prompt and skill text.
- Compute a similarity score from shared keywords.
- Trigger the highest-scoring skill above a defined threshold.

## Phase 3: Runtime execution

- Inject the skill instructions into the prompt before the model call.
- Keep the execution loop compatible with existing tools and approvals.

## Phase 4: Logging and traceability

- Write structured metadata into session memory.
- Keep an auditable list of prompt-to-skill matches for later inspection.

## Phase 5: Validation

- Run the existing test suite.
- Add focused tests covering skill discovery, matching, and logging.
