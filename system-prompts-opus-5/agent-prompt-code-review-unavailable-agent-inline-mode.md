<!--
name: 'Agent Prompt: /code-review unavailable-agent inline mode'
description: >-
  Builds a single-pass inline code-review prompt that gathers a diff, evaluates
  configured angles, deduplicates findings, optionally sweeps gaps, and reports
  capped results when the Agent tool is unavailable
ccVersion: 2.1.214
variables:
  - REVIEW_MODE_TAG
  - REVIEW_LEAD_IN
  - AGENT_UNAVAILABLE_INSTRUCTIONS
  - DIFF_GATHERING_PHASE
  - ANGLE_COUNT
  - FINDER_ANGLES_BLOCK
  - CLEANUP_AND_ALTITUDE_CANDIDATES_NOTE
  - GAP_SWEEP_PHASE
  - OUTPUT_FORMAT_FN
  - MAX_FINDINGS
  - INLINE_REVIEW_DISCLOSURE
-->
