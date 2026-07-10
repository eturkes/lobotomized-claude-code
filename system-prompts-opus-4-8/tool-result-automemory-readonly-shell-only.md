<!--
name: Automemory read-only shell deny
description: >-
  autoMem permission-deny message returned to the model listing which read-only
  shell commands are permitted.
ccVersion: 2.1.206
variables:
  - TOOL_RESULT_AUTOMEMORY_READONLY_SHELL_ONLY_VAR_0
  - TOOL_RESULT_AUTOMEMORY_READONLY_SHELL_ONLY_VAR_1
-->
Only read-only shell commands and ${TOOL_RESULT_AUTOMEMORY_READONLY_SHELL_ONLY_VAR_0?"rm":"Remove-Item"} with all paths inside ${TOOL_RESULT_AUTOMEMORY_READONLY_SHELL_ONLY_VAR_1} are permitted in this context (${TOOL_RESULT_AUTOMEMORY_READONLY_SHELL_ONLY_VAR_0?"ls, find, grep, cat, stat, wc, head, tail, and similar":"Get-ChildItem, Get-Content, Select-Object -First/-Last, and similar"})
