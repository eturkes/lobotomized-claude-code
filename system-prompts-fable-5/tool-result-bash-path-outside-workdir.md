<!--
name: Access blocked outside working directories
description: >-
  Command-safety block reason returned to the model when a command targets a
  path outside allowed working directories.
ccVersion: 2.1.206
variables:
  - TOOL_RESULT_BASH_PATH_OUTSIDE_WORKDIR_VAR_0
  - TOOL_RESULT_BASH_PATH_OUTSIDE_WORKDIR_VAR_1
  - TOOL_RESULT_BASH_PATH_OUTSIDE_WORKDIR_VAR_2
-->
${TOOL_RESULT_BASH_PATH_OUTSIDE_WORKDIR_VAR_0} targeting '${TOOL_RESULT_BASH_PATH_OUTSIDE_WORKDIR_VAR_1}' was blocked. For security, Claude Code may only access files in the allowed working directories for this session: ${TOOL_RESULT_BASH_PATH_OUTSIDE_WORKDIR_VAR_2}.
