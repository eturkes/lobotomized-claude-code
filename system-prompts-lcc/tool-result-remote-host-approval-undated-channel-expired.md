<!--
name: 'Tool Result: Remote host approval undated-channel expired'
description: >-
  Tells Claude a permission approval reached the target host over a channel that
  carries no delivery timestamp, arrived too long after the request was raised
  to be honored, so the request was withdrawn and nothing ran.
ccVersion: 2.1.284
variables:
  - TOOL_RESULT_REMOTE_HOST_APPROVAL_UNDATED_CHANNEL_EXPIRED_VAR_0
  - TOOL_RESULT_REMOTE_HOST_APPROVAL_UNDATED_CHANNEL_EXPIRED_VAR_1
  - TOOL_RESULT_REMOTE_HOST_APPROVAL_UNDATED_CHANNEL_EXPIRED_VAR_2
  - TOOL_RESULT_REMOTE_HOST_APPROVAL_UNDATED_CHANNEL_EXPIRED_VAR_3
-->
This approval reached ${TOOL_RESULT_REMOTE_HOST_APPROVAL_UNDATED_CHANNEL_EXPIRED_VAR_0} over a channel that carries no delivery time, ${TOOL_RESULT_REMOTE_HOST_APPROVAL_UNDATED_CHANNEL_EXPIRED_VAR_1} after the request was raised — longer than such an answer is honoured for (${TOOL_RESULT_REMOTE_HOST_APPROVAL_UNDATED_CHANNEL_EXPIRED_VAR_2} ${TOOL_RESULT_REMOTE_HOST_APPROVAL_UNDATED_CHANNEL_EXPIRED_VAR_3(TOOL_RESULT_REMOTE_HOST_APPROVAL_UNDATED_CHANNEL_EXPIRED_VAR_2,"hour")}) — so the request was withdrawn and nothing ran. Send the call again if it is still wanted.
