<!--
name: 'System Reminder: Dir Sync File Store Share Used Up'
description: >-
  Reminds the model that the cloud environment has used up its share of the
  session's file store (upload/byte counts) and changes stay cloud-side from now
  on.
ccVersion: 2.1.284
variables:
  - SYSTEM_REMINDER_DIR_SYNC_FILE_STORE_SHARE_USED_UP_VAR_0
  - SYSTEM_REMINDER_DIR_SYNC_FILE_STORE_SHARE_USED_UP_VAR_1
  - SYSTEM_REMINDER_DIR_SYNC_FILE_STORE_SHARE_USED_UP_VAR_2
  - SYSTEM_REMINDER_DIR_SYNC_FILE_STORE_SHARE_USED_UP_VAR_3
  - SYSTEM_REMINDER_DIR_SYNC_FILE_STORE_SHARE_USED_UP_VAR_4
-->
From now on Claude's changes stay in the cloud session and are not synced to this machine: the cloud environment has used its share of this session's file store (${SYSTEM_REMINDER_DIR_SYNC_FILE_STORE_SHARE_USED_UP_VAR_0(SYSTEM_REMINDER_DIR_SYNC_FILE_STORE_SHARE_USED_UP_VAR_1.links)} of ${SYSTEM_REMINDER_DIR_SYNC_FILE_STORE_SHARE_USED_UP_VAR_0(SYSTEM_REMINDER_DIR_SYNC_FILE_STORE_SHARE_USED_UP_VAR_2)} uploads, ${SYSTEM_REMINDER_DIR_SYNC_FILE_STORE_SHARE_USED_UP_VAR_3(SYSTEM_REMINDER_DIR_SYNC_FILE_STORE_SHARE_USED_UP_VAR_1.bytes)} of ${SYSTEM_REMINDER_DIR_SYNC_FILE_STORE_SHARE_USED_UP_VAR_3(SYSTEM_REMINDER_DIR_SYNC_FILE_STORE_SHARE_USED_UP_VAR_4)} MiB).
