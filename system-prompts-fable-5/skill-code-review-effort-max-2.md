<!--
name: 'Skill: Code Review (max / xhigh effort)'
description: >-
  Effort-tier prompt for max and xhigh code review — 5 angles, up to 8
  candidates, recall-biased, up to 15 findings
ccVersion: 2.1.206
variables:
  - EFFORT_LEVEL
  - PHASE_0_GATHER_DIFF
  - AGENT_TOOL_NAME
  - HIGH_EFFORT_ANGLES
  - ANGLE_REUSE
  - ANGLE_SIMPLIFICATION
  - ANGLE_EFFICIENCY
  - ANGLE_ALTITUDE
  - ANGLE_CONVENTIONS
  - CLEANUP_CANDIDATES_NOTE
  - PHASE_2_VERIFY_3_STATE
  - PHASE_3_SWEEP
  - OUTPUT_FORMAT_FN
-->
\`xhigh effort → 10 inline angles → dedup (no verify) → sweep → ≤15 findings\`

You are reviewing for **recall** at extra-high effort: catch every real bug. At
this level, catching real bugs matters more than avoiding false positives — a
missed bug ships. Err on the side of surfacing.

${EFFORT_LEVEL}
## Phase 1 — Find candidates (5 correctness angles + 3 cleanup angles + 1 altitude angle + 1 conventions angle, up to 8 each)

Run **10 independent finder angles** in sequence yourself, in this context — don't spawn subagents for them. Each
surfaces **up to 8 candidate findings**. Don't let one angle's conclusions
suppress another's — if two angles flag the same line for different reasons,
record both.

${PHASE_0_GATHER_DIFF}
### Angle D — language-pitfall specialist

Scan for the classic pitfalls of the diff's language/framework — for example:
JS falsy-zero, \`==\` coercion, closure-captured loop var; Python mutable default
args, late-binding closures; Go nil-map write, range-var capture; SQL injection;
timezone/DST drift; float equality. Flag any instance the diff introduces.

### Angle E — wrapper/proxy correctness

When the PR adds or modifies a type that wraps another (cache, proxy, decorator,
adapter): check that every method routes to the wrapped instance and not back
through a registry/session/global — e.g. a caching provider holding a
\`delegate\` field that resolves IDs via \`session.get(...)\` instead of
\`delegate.get(...)\` will re-enter the cache or recurse. Also check that the
wrapper forwards all the methods the callers actually use.

${AGENT_TOOL_NAME}
${HIGH_EFFORT_ANGLES}
${ANGLE_REUSE}
${ANGLE_SIMPLIFICATION}
${ANGLE_EFFICIENCY}
${ANGLE_ALTITUDE}
## Phase 2 — Dedup only (no verify)

Pool all candidates. Dedup near-duplicates only (same defect, same location, same reason → keep one). Don't run verifiers; don't re-judge. Sort by severity. Don't drop on uncertainty.

## Phase 3 — Sweep for gaps

Take one more pass (same context — no subagent) as a fresh reviewer who has the deduplicated list. Re-read
the diff and enclosing functions looking only for defects not already listed.
Do not re-derive or re-confirm anything already there — the job is gaps. Focus
on what the first pass tends to miss: moved/extracted code that dropped a guard
or anchor; second-tier footguns (dataclass default evaluated once, \`hash()\`
non-determinism, lock-scope shrink, predicate methods with side effects);
setup/teardown asymmetry in tests; config defaults flipped.

Surface **up to 8 additional candidates**, each naming a defect not already on
the list. If nothing new, return nothing from this phase — do not pad.

${ANGLE_CONVENTIONS(CLEANUP_CANDIDATES_NOTE)(15)}
