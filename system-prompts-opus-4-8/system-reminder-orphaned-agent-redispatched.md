<!--
name: Orphaned background agent (re-dispatched) notice
description: >-
  Notification injected into model context on resume when a re-dispatched
  background agent has no completion record.
ccVersion: 2.1.206
variables:
  - SYSTEM_REMINDER_ORPHANED_AGENT_REDISPATCHED_VAR_0
  - SYSTEM_REMINDER_ORPHANED_AGENT_REDISPATCHED_VAR_1
-->
No completion record was found for background agent "${SYSTEM_REMINDER_ORPHANED_AGENT_REDISPATCHED_VAR_0(SYSTEM_REMINDER_ORPHANED_AGENT_REDISPATCHED_VAR_1.description)}" after it was re-dispatched via SendMessage in the previous session. It may have been stopped (via the UI, an SDK interrupt, or agent teardown — these leave no transcript marker), or it may have been running when the previous Claude Code process exited. Check its worktree/output for partial work before assuming the task landed.
