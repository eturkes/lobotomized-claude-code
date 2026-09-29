<!--
name: 'System Reminder: Dir Sync Cloud Checkout Unready Not Sent'
description: >-
  Reminds the model that this turn's changes were not sent because the cloud
  checkout is unreadable/mid-operation/unborn/conflicted, retried after
  resolution.
ccVersion: 2.1.284
variables:
  - SYSTEM_REMINDER_DIR_SYNC_CLOUD_CHECKOUT_UNREADY_NOT_SENT_VAR_0
-->
Claude's changes from this turn were not sent: the cloud checkout is ${SYSTEM_REMINDER_DIR_SYNC_CLOUD_CHECKOUT_UNREADY_NOT_SENT_VAR_0.condition==="unreadable"?"not readable just now":SYSTEM_REMINDER_DIR_SYNC_CLOUD_CHECKOUT_UNREADY_NOT_SENT_VAR_0.condition==="mid_operation"?"in the middle of a merge, rebase or cherry-pick":SYSTEM_REMINDER_DIR_SYNC_CLOUD_CHECKOUT_UNREADY_NOT_SENT_VAR_0.condition==="unborn"?"without a commit":"holding unresolved merge conflicts"}; they go out with the first turn after that is resolved.
