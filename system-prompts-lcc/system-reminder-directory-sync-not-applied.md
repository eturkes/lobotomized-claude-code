<!--
name: 'System Reminder: directory sync not applied this turn'
description: >-
  Tells Claude the user's latest changes were not applied to this checkout this
  turn, with a reason, and that sync retries next turn.
ccVersion: 2.1.284
variables:
  - SYSTEM_REMINDER_DIRECTORY_SYNC_NOT_APPLIED_VAR_0
  - SYSTEM_REMINDER_DIRECTORY_SYNC_NOT_APPLIED_VAR_1
-->
Directory sync: the user's latest changes were NOT applied to this checkout this turn because ${SYSTEM_REMINDER_DIRECTORY_SYNC_NOT_APPLIED_VAR_0(SYSTEM_REMINDER_DIRECTORY_SYNC_NOT_APPLIED_VAR_1.reason,SYSTEM_REMINDER_DIRECTORY_SYNC_NOT_APPLIED_VAR_1.detail)}; the checkout is unchanged and sync retries at the next turn. If the user refers to edits you cannot see, that is why.
