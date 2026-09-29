<!--
name: 'System Reminder: directory sync service not answering'
description: >-
  Tells Claude the directory-sync service is not answering at turn-arming time
  and keeps retrying.
ccVersion: 2.1.284
variables:
  - SYSTEM_REMINDER_DIRECTORY_SYNC_SERVICE_NOT_ANSWERING_VAR_0
-->
Directory sync ${SYSTEM_REMINDER_DIRECTORY_SYNC_SERVICE_NOT_ANSWERING_VAR_0.resuming?"has not resumed in this session yet (this process restarted)":"has not started for this session yet"}: the sync service is not answering. It keeps trying at each turn; until then the user's changes are not arriving here and yours are not going up.
