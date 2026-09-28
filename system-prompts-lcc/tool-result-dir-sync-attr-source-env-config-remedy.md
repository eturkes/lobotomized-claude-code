<!--
name: 'Dir-sync: attribute-source env/config setting cannot follow'
description: >-
  Explains that an environment or config-derived setting can change which git
  attribute rules apply in a way dir-sync cannot follow, and tells the user to
  remove it and start a new cloud session.
ccVersion: 2.1.284
variables:
  - TOOL_RESULT_DIR_SYNC_ATTR_SOURCE_ENV_CONFIG_REMEDY_VAR_0
  - TOOL_RESULT_DIR_SYNC_ATTR_SOURCE_ENV_CONFIG_REMEDY_VAR_1
-->
${TOOL_RESULT_DIR_SYNC_ATTR_SOURCE_ENV_CONFIG_REMEDY_VAR_0} in ${TOOL_RESULT_DIR_SYNC_ATTR_SOURCE_ENV_CONFIG_REMEDY_VAR_1} can change which attribute rules git applies, in a way sync cannot follow; remove it from your shell or Claude Code settings, then restart Claude Code and start a new cloud session
