# GYM-TRAKER

## WHAT
- Purpose: track all workouts and generate training plans based on physical effort and goals. Later: nutrition tracking.
- Tech stack: TBD (to be decided in the planning phase).
- Repo: github.com/Titoflow68/GYM-TRAKER (PUBLIC).
- Folder map:
  - `src/` source code
  - `tests/` tests
  - `data/` personal workout/nutrition data (gitignored); `data/state/` script memory (last run, processed IDs)
  - `.tmp/` ephemeral generated files (gitignored)
  - `.claude/` rules, agents, hooks, skills, worktrees

## HOW
- Build/run/test commands: TBD.
- Python env: `python -m venv .venv && source .venv/bin/activate`.
- API keys: in `.env` (gitignored). Variable names: TBD.

## WHY
- Personal data lives in `data/`, never in git: the repo is public and the data is health-related.
- Decisions will be logged here as the architecture is defined.

## DON'TS
- Never read or display `.env`; cite variable names only.
- Never commit personal health data, credentials or tokens.
- Do not edit files outside the current task.

## Adaptive Guardrails

Scan every entry below before starting any task. No exceptions.

This is a living correction log. When the user corrects you, or when a wrong assumption causes a bug, append a new entry immediately. Entries are permanent -- never delete, only supersede.

### Entry format

N. [ACTIVATION] Directive -- reason.

- **N**: Sequential number. Never reuse.
- **ACTIVATION**: One of three modes:
  - `ALWAYS` -- Applies to every task unconditionally. Internalize before doing anything.
  - `NEVER` -- Hard prohibition. Zero tolerance, zero exceptions.
  - `WHEN:surface` -- Fires only when working with a specific surface. Examples: `WHEN:video`, `WHEN:api`, `WHEN:frontend`. Skip if the surface isn't part of the current task.

### Recording entries

Append when:
- The user rejects your output or redirects your approach
- A bug traces to an incorrect assumption about this codebase
- The user declares a standing preference

Do not record one-off instructions. Only permanent patterns or explicit standing orders.

### Resolving contradictions

When two entries clash, apply in order:
1. **Supersession** -- an entry ending with `(supersedes #N)` kills entry N. Dead entries stay visible but are ignored.
2. **Specificity** -- `WHEN:api` beats `ALWAYS` on API tasks. Narrower scope wins.
3. **Recency** -- higher entry number wins. Last resort only.

### Correction Log

(empty -- entries will accumulate as you work)
