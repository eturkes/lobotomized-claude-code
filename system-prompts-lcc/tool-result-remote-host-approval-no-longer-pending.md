<!--
name: 'Tool Result: Remote host approval no longer pending'
description: >-
  Tells Claude a permission answer for a remote-tool call is no longer pending
  on the target host, so nothing ran, and to send the call again without an
  approval to ask afresh.
ccVersion: 2.1.284
variables:
  - TOOL_RESULT_REMOTE_HOST_APPROVAL_NO_LONGER_PENDING_VAR_0
-->
That permission request is no longer pending on ${TOOL_RESULT_REMOTE_HOST_APPROVAL_NO_LONGER_PENDING_VAR_0.targetName} — nothing ran. Send the call again without an approval to ask afresh.
