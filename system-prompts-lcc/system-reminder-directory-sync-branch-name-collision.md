<!--
name: 'System Reminder: Directory sync branch name collision'
description: >-
  Reports that directory sync could not create the user's branch because another
  local branch occupies a conflicting git ref path
ccVersion: 2.1.284
variables:
  - BLOCKING_BRANCH_NAME
  - SYSTEM_REMINDER_DIRECTORY_SYNC_BRANCH_NAME_COLLISION_VAR_1
-->
Directory sync: the user's latest changes were NOT applied because the user is now on a branch that cannot be created in THIS checkout while another branch here occupies part of its name — git stores branches as paths, so "feature" and "feature/v2" cannot coexist: ${BLOCKING_BRANCH_NAME(SYSTEM_REMINDER_DIRECTORY_SYNC_BRANCH_NAME_COLLISION_VAR_1.detail??"a branch of this checkout")}. Rename or delete the branch of this checkout that is in the way (git branch -m OLD OTHER-NAME, or git branch -D OLD if its commits are merged or parked), tell the user you did, and sync resumes at the next turn. Nothing in the checkout was changed.
