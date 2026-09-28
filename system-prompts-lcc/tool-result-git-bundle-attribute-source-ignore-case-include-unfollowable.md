<!--
name: 'Tool Result: Git bundle attribute source ignoreCase include unfollowable'
description: >-
  Tells the agent an included git config sets a case-matching option file sync
  cannot follow, with the fix of moving the setting.
ccVersion: 2.1.284
variables:
  - >-
    TOOL_RESULT_GIT_BUNDLE_ATTRIBUTE_SOURCE_IGNORE_CASE_INCLUDE_UNFOLLOWABLE_VAR_0
-->
A file your git configuration includes sets ${TOOL_RESULT_GIT_BUNDLE_ATTRIBUTE_SOURCE_IGNORE_CASE_INCLUDE_UNFOLLOWABLE_VAR_0}, which can change how git matches attribute rules in a way file sync cannot follow, so a file git changes before storing it could be uploaded as it is on disk. Move the setting from the included file into the git configuration of each project it is meant for, or into your own git configuration file.
