<!--
name: Orphaned background agent (state lost) notice
description: >-
  Notification injected into model context on resume about a background agent
  that was running at exit and lost its in-process state.
ccVersion: 2.1.206
variables:
  - SYSTEM_REMINDER_ORPHANED_AGENT_LOST_VAR_0
  - SYSTEM_REMINDER_ORPHANED_AGENT_LOST_VAR_1
-->
Background agent "${SYSTEM_REMINDER_ORPHANED_AGENT_LOST_VAR_0(SYSTEM_REMINDER_ORPHANED_AGENT_LOST_VAR_1.description)}" was running when the previous Claude Code process exited and did not complete. Its in-process state was lost. Check its worktree/output for partial work before assuming the task landed.
