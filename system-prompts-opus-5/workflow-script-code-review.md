<!--
name: 'Workflow Script: /code-review'
description: >-
  Bundled /code-review workflow — scopes the diff, fans out per-angle finders,
  dedups, verifies, sweeps for gaps (xhigh/max), and synthesizes;
  effort-parameterized via LEVEL_PARAMS
ccVersion: 2.1.199
variables:
  - JSON
  - WORKFLOW_NAME
  - WORKFLOW_DESCRIPTION
  - WORKFLOW_WHEN_TO_USE
  - WORKFLOW_PHASES
  - CORRECTNESS_ANGLES
  - CLEANUP_ANGLES
  - VERDICT_LADDER
  - VERDICT_LADDER_RECALL
  - CLEANUP_PRECEDENCE
  - SWEEP_GAP_FOCUS
-->
