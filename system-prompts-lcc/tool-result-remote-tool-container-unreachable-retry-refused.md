<!--
name: 'Tool Result: remote/container tool unreachable, retry refused this turn'
description: >-
  Text telling Claude not to call an unreachable attached-machine/container tool
  again this turn, to do the rest of the task it can, tell the user what is
  blocked, and only check again when the user says it is back
ccVersion: 2.1.284
variables:
  - TOOL_RESULT_REMOTE_TOOL_CONTAINER_UNREACHABLE_RETRY_REFUSED_VAR_0
  - TOOL_RESULT_REMOTE_TOOL_CONTAINER_UNREACHABLE_RETRY_REFUSED_VAR_1
-->
${TOOL_RESULT_REMOTE_TOOL_CONTAINER_UNREACHABLE_RETRY_REFUSED_VAR_0} Do not call ${TOOL_RESULT_REMOTE_TOOL_CONTAINER_UNREACHABLE_RETRY_REFUSED_VAR_1} again in this turn: do the rest of the task that this container can do, and tell the user what is blocked. Check once more only when the user says it is back or asks you to try again.
