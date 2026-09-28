<!--
name: 'System Reminder: dir sync environment replaced, partial restore'
description: >-
  Tells Claude its cloud environment's earlier work could be restored only in
  part after a container replacement.
ccVersion: 2.1.284
variables:
  - SYSTEM_REMINDER_DIR_SYNC_ENVIRONMENT_REPLACED_PARTIAL_RESTORE_VAR_0
  - SYSTEM_REMINDER_DIR_SYNC_ENVIRONMENT_REPLACED_PARTIAL_RESTORE_VAR_1
  - SYSTEM_REMINDER_DIR_SYNC_ENVIRONMENT_REPLACED_PARTIAL_RESTORE_VAR_2
  - SYSTEM_REMINDER_DIR_SYNC_ENVIRONMENT_REPLACED_PARTIAL_RESTORE_VAR_3
-->
Directory sync: ${SYSTEM_REMINDER_DIR_SYNC_ENVIRONMENT_REPLACED_PARTIAL_RESTORE_VAR_0} and your earlier work could be RESTORED into this checkout only IN PART — up to ${SYSTEM_REMINDER_DIR_SYNC_ENVIRONMENT_REPLACED_PARTIAL_RESTORE_VAR_1}; your work after that could not be brought back (${SYSTEM_REMINDER_DIR_SYNC_ENVIRONMENT_REPLACED_PARTIAL_RESTORE_VAR_2[e.why]}) and is NOT here. It comes back only through the user's machine, if it had reached it (its upload for this turn may already have brought it) — check the files before building on them rather than redoing that work from memory, and tell the user plainly which recent changes are missing if they matter now. Not restored either: untracked files sync never carries, ${SYSTEM_REMINDER_DIR_SYNC_ENVIRONMENT_REPLACED_PARTIAL_RESTORE_VAR_3}.
