# Project memory instructions

This repository keeps project memory in `agent-memory/`. The memory helps an agent find relevant project context across sessions; it is not a replacement for the project's source files or specifications.

## At the start of a task

1. Read `agent-memory/index.md`.
2. Open only the memory pages and source files relevant to the task.
3. Check the current project files before relying on remembered implementation details.

Do not load the whole memory directory by default. Follow links in the index and expand only when the task needs more context.

## Source of truth

Use this order when information conflicts:

1. The user's current explicit instruction.
2. Current checked-in project files and canonical design specifications.
3. Confirmed decision records, if they still match the current project.
4. Lessons and handoff notes.
5. Agent inference.

Memory records explain intent and history. The actual project files define the current implementation. If a decision is superseded, mark it as such and link to the newer record; do not silently rewrite history.

## When to update memory

Record information when it is likely to matter in a later session:

- A user explicitly confirms a durable project decision.
- A non-obvious constraint or recurring pitfall is discovered.
- A source of truth moves or its role changes.
- Work is being handed off while incomplete.

Do not record transient conversation details, guesses, credentials, tokens, personal data, or information unrelated to this public project. This repository is public; keep private preferences in a private location.

When adding or changing a memory page:

1. Include its status, date when known, scope, and source or evidence.
2. Update `agent-memory/index.md` so the page is discoverable.
3. Append a concise entry to `agent-memory/log.md` for meaningful memory-system changes.
4. Keep `agent-memory/handoff.md` limited to the currently active handoff; clear or replace it when that handoff ends.

## Project-specific sources

The design system package is under `esther-design-system-earthy-palette/esther-design-system-main/`. Its `SKILL.md`, `brand-dna.md`, and `references/` files are canonical project guidance. Read the relevant source directly before making design-system changes; do not duplicate its detailed rules into memory.
