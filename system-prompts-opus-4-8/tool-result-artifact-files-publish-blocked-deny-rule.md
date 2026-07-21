<!--
name: 'Tool result: Artifact files publish blocked by deny rule'
description: >-
  Hard-deny message when a source file to publish is blocked by a Read deny
  rule, returned to the model as the block reason.
ccVersion: null
variables:
  - TOOL_RESULT_ARTIFACT_FILES_PUBLISH_BLOCKED_DENY_RULE_VAR_0
  - TOOL_RESULT_ARTIFACT_FILES_PUBLISH_BLOCKED_DENY_RULE_VAR_1
-->
files: publishing ${TOOL_RESULT_ARTIFACT_FILES_PUBLISH_BLOCKED_DENY_RULE_VAR_0.stringify(TOOL_RESULT_ARTIFACT_FILES_PUBLISH_BLOCKED_DENY_RULE_VAR_1.from)} is blocked by a Read permission rule
