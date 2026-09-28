<!--
name: 'System Reminder: Dir Sync Cloud Branch Name Collides Rename'
description: >-
  Tells the model the cloud checkout has a branch name collision blocking apply,
  and that it was asked to rename/delete the colliding branch there.
ccVersion: 2.1.284
variables:
  - SYSTEM_REMINDER_DIR_SYNC_CLOUD_BRANCH_NAME_COLLIDES_RENAME_VAR_0
  - SYSTEM_REMINDER_DIR_SYNC_CLOUD_BRANCH_NAME_COLLIDES_RENAME_VAR_1
-->
Your latest changes were not applied in the cloud session: its checkout still has a branch whose name cannot coexist in git with the branch you are on now (${SYSTEM_REMINDER_DIR_SYNC_CLOUD_BRANCH_NAME_COLLIDES_RENAME_VAR_0===void 0?"named in the session":SYSTEM_REMINDER_DIR_SYNC_CLOUD_BRANCH_NAME_COLLIDES_RENAME_VAR_1(SYSTEM_REMINDER_DIR_SYNC_CLOUD_BRANCH_NAME_COLLIDES_RENAME_VAR_0)}); Claude was asked to rename or delete that branch in the cloud checkout, after which sync resumes.
