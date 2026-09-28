<!--
name: 'System Reminder: Directory sync trash files not moved back clause'
description: >-
  Clause telling the agent some of its files were moved into the sync trash
  folder to make room and are still there.
ccVersion: 2.1.284
variables:
  - SYSTEM_REMINDER_DIR_SYNC_TRASH_FILES_NOT_MOVED_BACK_CLAUSE_VAR_0
  - SYSTEM_REMINDER_DIR_SYNC_TRASH_FILES_NOT_MOVED_BACK_CLAUSE_VAR_1
  - SYSTEM_REMINDER_DIR_SYNC_TRASH_FILES_NOT_MOVED_BACK_CLAUSE_VAR_2
-->
; some of your files had already been moved into the trash folder ${SYSTEM_REMINDER_DIR_SYNC_TRASH_FILES_NOT_MOVED_BACK_CLAUSE_VAR_0(SYSTEM_REMINDER_DIR_SYNC_TRASH_FILES_NOT_MOVED_BACK_CLAUSE_VAR_1.trash)} to make room, and could not be moved back, so they are still there: ${SYSTEM_REMINDER_DIR_SYNC_TRASH_FILES_NOT_MOVED_BACK_CLAUSE_VAR_2(SYSTEM_REMINDER_DIR_SYNC_TRASH_FILES_NOT_MOVED_BACK_CLAUSE_VAR_1.moved,SYSTEM_REMINDER_DIR_SYNC_TRASH_FILES_NOT_MOVED_BACK_CLAUSE_VAR_1.trash)}
