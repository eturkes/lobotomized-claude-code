<!--
name: Approval answers a different request
description: >-
  tool_result message when an approval answers a different request than the one
  pending on the target; nothing ran, caller told to send the call without an
  approval to ask afresh.
ccVersion: 2.1.284
variables:
  - TOOL_RESULT_REMOTE_TOOL_APPROVAL_ANSWERS_DIFFERENT_REQUEST_VAR_0
-->
This approval answers a different request than the one pending on ${TOOL_RESULT_REMOTE_TOOL_APPROVAL_ANSWERS_DIFFERENT_REQUEST_VAR_0.targetName} — nothing ran. Send the call without an approval to ask afresh.
