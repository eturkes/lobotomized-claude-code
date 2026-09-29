<!--
name: 'Dir-sync: branch not put back, index still old (reused suffix)'
description: >-
  Reusable suffix template describing that a branch was not put back and may
  still name the session's HEAD while the index is the old one, with a
  remediation command; appears twice with different prefixes describing what
  happened to the branch.
ccVersion: 2.1.284
variables:
  - TOOL_RESULT_DIR_SYNC_BRANCH_NOT_PUT_BACK_INDEX_OLD_VAR_0
  - TOOL_RESULT_DIR_SYNC_BRANCH_NOT_PUT_BACK_INDEX_OLD_VAR_1
  - TOOL_RESULT_DIR_SYNC_BRANCH_NOT_PUT_BACK_INDEX_OLD_VAR_2
  - TOOL_RESULT_DIR_SYNC_BRANCH_NOT_PUT_BACK_INDEX_OLD_VAR_3
  - TOOL_RESULT_DIR_SYNC_BRANCH_NOT_PUT_BACK_INDEX_OLD_VAR_4
-->
${TOOL_RESULT_DIR_SYNC_BRANCH_NOT_PUT_BACK_INDEX_OLD_VAR_0}, and the branch was not put back (it may never have moved); if it names the session's HEAD while the index is still the old one, ${TOOL_RESULT_DIR_SYNC_BRANCH_NOT_PUT_BACK_INDEX_OLD_VAR_1(TOOL_RESULT_DIR_SYNC_BRANCH_NOT_PUT_BACK_INDEX_OLD_VAR_2,TOOL_RESULT_DIR_SYNC_BRANCH_NOT_PUT_BACK_INDEX_OLD_VAR_3,TOOL_RESULT_DIR_SYNC_BRANCH_NOT_PUT_BACK_INDEX_OLD_VAR_4)}
