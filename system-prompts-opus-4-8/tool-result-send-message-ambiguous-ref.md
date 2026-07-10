<!--
name: Ambiguous recipient
description: >-
  SendMessage tool-error returned to the model when a name matches multiple
  agents.
ccVersion: 2.1.206
variables:
  - TOOL_RESULT_SEND_MESSAGE_AMBIGUOUS_REF_VAR_0
  - TOOL_RESULT_SEND_MESSAGE_AMBIGUOUS_REF_VAR_1
-->
'${TOOL_RESULT_SEND_MESSAGE_AMBIGUOUS_REF_VAR_0.to}' matches ${TOOL_RESULT_SEND_MESSAGE_AMBIGUOUS_REF_VAR_1.total} agents. Re-send with the ref:
