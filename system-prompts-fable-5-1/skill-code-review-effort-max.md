<!--
name: 'Skill: Code Review (xhigh effort, inline single-pass)'
description: >-
  Effort-tier prompt for the inline xhigh code review — 10 angles run in-context
  with no subagents, dedup only (no verify), sweep, up to 15 findings. Reshaped
  in 2.1.214; the fan-out variant now lives in skill-code-review-effort-max-3.
ccVersion: 2.1.218
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

