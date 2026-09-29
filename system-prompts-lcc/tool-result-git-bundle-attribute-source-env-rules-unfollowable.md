<!--
name: 'Tool Result: Git bundle attribute source env rules unfollowable'
description: >-
  Tells the agent an environment git setting changes attribute rules in a way
  file sync cannot follow, so a filtered file could upload as on disk.
ccVersion: 2.1.284
variables:
  - TOOL_RESULT_GIT_BUNDLE_ATTRIBUTE_SOURCE_ENV_RULES_UNFOLLOWABLE_VAR_0
  - TOOL_RESULT_GIT_BUNDLE_ATTRIBUTE_SOURCE_ENV_RULES_UNFOLLOWABLE_VAR_1
-->
${TOOL_RESULT_GIT_BUNDLE_ATTRIBUTE_SOURCE_ENV_RULES_UNFOLLOWABLE_VAR_0} sets ${TOOL_RESULT_GIT_BUNDLE_ATTRIBUTE_SOURCE_ENV_RULES_UNFOLLOWABLE_VAR_1}, which can change the attribute rules git applies, in a way file sync cannot follow, so a file git changes before storing it could be uploaded as it is on disk. Remove it from your shell or your Claude Code settings.
