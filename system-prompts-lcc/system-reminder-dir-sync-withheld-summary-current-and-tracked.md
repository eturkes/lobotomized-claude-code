<!--
name: 'Dir sync: withheld summary (current contents and tracked history)'
description: >-
  Summary reminder sentence listing files whose current contents were left on
  the machine plus every version of git-tracked files that must stay, explaining
  the session runs without them.
ccVersion: 2.1.284
variables:
  - SYSTEM_REMINDER_DIR_SYNC_WITHHELD_SUMMARY_CURRENT_AND_TRACKED_VAR_0
  - SYSTEM_REMINDER_DIR_SYNC_WITHHELD_SUMMARY_CURRENT_AND_TRACKED_VAR_1
  - SYSTEM_REMINDER_DIR_SYNC_WITHHELD_SUMMARY_CURRENT_AND_TRACKED_VAR_2
  - SYSTEM_REMINDER_DIR_SYNC_WITHHELD_SUMMARY_CURRENT_AND_TRACKED_VAR_3
-->
Left on this machine: the current contents of ${SYSTEM_REMINDER_DIR_SYNC_WITHHELD_SUMMARY_CURRENT_AND_TRACKED_VAR_0.join(", ")}, and every version of ${SYSTEM_REMINDER_DIR_SYNC_WITHHELD_SUMMARY_CURRENT_AND_TRACKED_VAR_1}; the session runs without ${SYSTEM_REMINDER_DIR_SYNC_WITHHELD_SUMMARY_CURRENT_AND_TRACKED_VAR_2(SYSTEM_REMINDER_DIR_SYNC_WITHHELD_SUMMARY_CURRENT_AND_TRACKED_VAR_3,"that one",`those ${SYSTEM_REMINDER_DIR_SYNC_WITHHELD_SUMMARY_CURRENT_AND_TRACKED_VAR_3}`)} and starts with the version git already holds for each of the others, or without it.
