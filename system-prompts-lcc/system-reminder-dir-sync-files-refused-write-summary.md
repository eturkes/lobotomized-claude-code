<!--
name: 'Dir-sync: files Claude changed refused summary line'
description: >-
  Summary line reporting how many files Claude changed of a given reason (e.g.
  could not be written here and stayed as they were), listed by path, as part of
  the dir-sync file-sync status reminder shown after a sync.
ccVersion: 2.1.284
variables:
  - SYSTEM_REMINDER_DIR_SYNC_FILES_REFUSED_WRITE_SUMMARY_VAR_0
  - SYSTEM_REMINDER_DIR_SYNC_FILES_REFUSED_WRITE_SUMMARY_VAR_1
  - SYSTEM_REMINDER_DIR_SYNC_FILES_REFUSED_WRITE_SUMMARY_VAR_2
-->
${SYSTEM_REMINDER_DIR_SYNC_FILES_REFUSED_WRITE_SUMMARY_VAR_0} Claude changed ${SYSTEM_REMINDER_DIR_SYNC_FILES_REFUSED_WRITE_SUMMARY_VAR_1[r]??"could not be written here and stayed as they were"}: ${SYSTEM_REMINDER_DIR_SYNC_FILES_REFUSED_WRITE_SUMMARY_VAR_2}
