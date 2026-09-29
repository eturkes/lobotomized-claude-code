<!--
name: 'System Reminder: Directory sync environment replaced, work restored'
description: >-
  Tells the agent its cloud container was recreated and its commits, staged
  state and working files were fully restored. Lists what was not restored:
  other branches, stashes, untracked files, tools and processes.
ccVersion: 2.1.284
variables:
  - SYSTEM_REMINDER_DIRECTORY_SYNC_ENVIRONMENT_REPLACED_WORK_RESTORED_VAR_0
  - SYSTEM_REMINDER_DIRECTORY_SYNC_ENVIRONMENT_REPLACED_WORK_RESTORED_VAR_1
  - SYSTEM_REMINDER_DIRECTORY_SYNC_ENVIRONMENT_REPLACED_WORK_RESTORED_VAR_2
  - SYSTEM_REMINDER_DIRECTORY_SYNC_ENVIRONMENT_REPLACED_WORK_RESTORED_VAR_3
  - SYSTEM_REMINDER_DIRECTORY_SYNC_ENVIRONMENT_REPLACED_WORK_RESTORED_VAR_4
-->
Directory sync: ${SYSTEM_REMINDER_DIRECTORY_SYNC_ENVIRONMENT_REPLACED_WORK_RESTORED_VAR_0} and your earlier work was RESTORED into this checkout: your commits, the staged state and the working files, including uncommitted ones, are as they stood ${SYSTEM_REMINDER_DIRECTORY_SYNC_ENVIRONMENT_REPLACED_WORK_RESTORED_VAR_1} (${SYSTEM_REMINDER_DIRECTORY_SYNC_ENVIRONMENT_REPLACED_WORK_RESTORED_VAR_2.branch===null?"at the commit you had checked out":"on the branch you had checked out"}; ${SYSTEM_REMINDER_DIRECTORY_SYNC_ENVIRONMENT_REPLACED_WORK_RESTORED_VAR_3}); the user's newer changes, if any, are brought in as at any turn start. Anything you changed after that last upload is not here, and this notice cannot tell whether there was anything — check the files you last touched before building on them. What was NOT restored: untracked files sync never carries (dot-led paths such as a .env you wrote, dependency and build-output directories, credential-named or oversize files, nested repositories), anything outside the project directory, and ${SYSTEM_REMINDER_DIRECTORY_SYNC_ENVIRONMENT_REPLACED_WORK_RESTORED_VAR_4} — reinstall or restart what you need before relying on it, and do not assume a server or watcher you started earlier is still running.
