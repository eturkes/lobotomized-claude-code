<!--
name: Orphaned agents aggregate — stopped
description: >-
  Aggregate system-reminder listing background agents from a previous session
  with no completion record (stopped variant), injected as a task-notification
  into the model context.
ccVersion: 2.1.210
variables:
  - SYSTEM_REMINDER_ORPHANED_AGENTS_AGGREGATE_STOPPED_COUNT_VAR_0
  - SYSTEM_REMINDER_ORPHANED_AGENTS_AGGREGATE_STOPPED_COUNT_VAR_1
-->
No completion record was found for ${SYSTEM_REMINDER_ORPHANED_AGENTS_AGGREGATE_STOPPED_COUNT_VAR_0.length} background agents from the previous session: ${SYSTEM_REMINDER_ORPHANED_AGENTS_AGGREGATE_STOPPED_COUNT_VAR_1}. They may have been stopped, or they may have been running when the previous Claude Code process exited — either way their transcripts are saved on disk, so their progress is not lost. Resume any of them by sending a message to its id with SendMessage, or check its worktree/output for partial work before assuming the task landed.
