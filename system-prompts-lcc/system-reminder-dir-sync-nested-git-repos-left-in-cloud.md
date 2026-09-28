<!--
name: 'System Reminder: Dir Sync Nested Git Repos Left In Cloud'
description: >-
  Reminds the model that nested git repositories inside the project are never
  entered by sync and stay in the cloud only.
ccVersion: 2.1.284
variables:
  - SYSTEM_REMINDER_DIR_SYNC_NESTED_GIT_REPOS_LEFT_IN_CLOUD_VAR_0
  - SYSTEM_REMINDER_DIR_SYNC_NESTED_GIT_REPOS_LEFT_IN_CLOUD_VAR_1
  - SYSTEM_REMINDER_DIR_SYNC_NESTED_GIT_REPOS_LEFT_IN_CLOUD_VAR_2
-->
Not synced — file sync never enters a git repository nested inside the project, so its files stay in the cloud: ${SYSTEM_REMINDER_DIR_SYNC_NESTED_GIT_REPOS_LEFT_IN_CLOUD_VAR_0.slice(0,SYSTEM_REMINDER_DIR_SYNC_NESTED_GIT_REPOS_LEFT_IN_CLOUD_VAR_1).map(SYSTEM_REMINDER_DIR_SYNC_NESTED_GIT_REPOS_LEFT_IN_CLOUD_VAR_2).join(", ")}${SYSTEM_REMINDER_DIR_SYNC_NESTED_GIT_REPOS_LEFT_IN_CLOUD_VAR_0.length>SYSTEM_REMINDER_DIR_SYNC_NESTED_GIT_REPOS_LEFT_IN_CLOUD_VAR_1?` and ${SYSTEM_REMINDER_DIR_SYNC_NESTED_GIT_REPOS_LEFT_IN_CLOUD_VAR_0.length-SYSTEM_REMINDER_DIR_SYNC_NESTED_GIT_REPOS_LEFT_IN_CLOUD_VAR_1} more`:""} (${SYSTEM_REMINDER_DIR_SYNC_NESTED_GIT_REPOS_LEFT_IN_CLOUD_VAR_0.length===1?"a repository":"repositories"} Claude cloned or created there).
