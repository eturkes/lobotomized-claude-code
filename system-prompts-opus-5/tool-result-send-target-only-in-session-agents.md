<!--
name: Send target matches only in-session agents
description: >-
  Refused-target SendFile result when a recipient matches only in-session
  agents, steering to reference the file as @<path>.
ccVersion: 2.1.210
variables:
  - TOOL_RESULT_SEND_TARGET_ONLY_IN_SESSION_AGENTS_VAR_0
  - TOOL_RESULT_SEND_TARGET_ONLY_IN_SESSION_AGENTS_VAR_1
-->
'${TOOL_RESULT_SEND_TARGET_ONLY_IN_SESSION_AGENTS_VAR_0}' matches only agents in this session — use ${TOOL_RESULT_SEND_TARGET_ONLY_IN_SESSION_AGENTS_VAR_1} and reference the file as @<path> instead.
