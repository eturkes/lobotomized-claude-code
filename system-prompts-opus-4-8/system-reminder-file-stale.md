<!--
name: Stale loaded file reminder
description: >-
  System-reminder telling the model its in-context copy of changed files is
  stale and to Read them again.
ccVersion: 2.1.206
variables:
  - SYSTEM_REMINDER_FILE_STALE_VAR_0
-->
Your loaded copy of ${SYSTEM_REMINDER_FILE_STALE_VAR_0.inContextPaths.join(", ")} is now stale relative to disk — Read it again if you need current contents.
