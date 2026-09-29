<!--
name: 'Dir-sync: ignore-case setting in included file'
description: >-
  Explains that dir-sync cannot follow an ignore-case-affecting setting found in
  an included git config file, and suggests moving it into each repository's own
  .git/config or the user's ~/.gitconfig.
ccVersion: 2.1.284
variables:
  - TOOL_RESULT_DIR_SYNC_IGNORE_CASE_INCLUDED_FILE_VAR_0
-->
sync cannot follow ${TOOL_RESULT_DIR_SYNC_IGNORE_CASE_INCLUDED_FILE_VAR_0} in an included file; move it into the .git/config of each repository it is meant for, or into your ~/.gitconfig
