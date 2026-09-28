<!--
name: 'System Reminder: Dir Sync Kept In Cloud Only List'
description: >-
  Lists files/dirs kept in the cloud session only because sync never carries
  dot-led paths, dependency/build dirs, temp files, or credential-like names.
ccVersion: 2.1.284
variables:
  - SYSTEM_REMINDER_DIR_SYNC_KEPT_IN_CLOUD_ONLY_LIST_VAR_0
  - SYSTEM_REMINDER_DIR_SYNC_KEPT_IN_CLOUD_ONLY_LIST_VAR_1
  - SYSTEM_REMINDER_DIR_SYNC_KEPT_IN_CLOUD_ONLY_LIST_VAR_2
  - SYSTEM_REMINDER_DIR_SYNC_KEPT_IN_CLOUD_ONLY_LIST_VAR_3
  - SYSTEM_REMINDER_DIR_SYNC_KEPT_IN_CLOUD_ONLY_LIST_VAR_4
-->
Kept in the cloud session only (sync never carries dot-led paths, dependency or build-output directories, editor or temporary files, or credential-like and other withheld names to your machine): ${[SYSTEM_REMINDER_DIR_SYNC_KEPT_IN_CLOUD_ONLY_LIST_VAR_0,SYSTEM_REMINDER_DIR_SYNC_KEPT_IN_CLOUD_ONLY_LIST_VAR_1.length>0?SYSTEM_REMINDER_DIR_SYNC_KEPT_IN_CLOUD_ONLY_LIST_VAR_2:"",SYSTEM_REMINDER_DIR_SYNC_KEPT_IN_CLOUD_ONLY_LIST_VAR_3].filter(SYSTEM_REMINDER_DIR_SYNC_KEPT_IN_CLOUD_ONLY_LIST_VAR_4).join("; and ")}.
