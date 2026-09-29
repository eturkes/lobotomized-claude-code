<!--
name: Deadline reached during file sync (pre-start)
description: >-
  tool_result message for a call whose admission deadline was reached while file
  sync was still writing the cloud session's newer files into the checkout,
  before the command started; nothing ran.
ccVersion: 2.1.284
variables:
  - TOOL_RESULT_REMOTE_TOOL_DEADLINE_REACHED_DURING_FILE_SYNC_VAR_0
-->
The call reached its deadline on ${TOOL_RESULT_REMOTE_TOOL_DEADLINE_REACHED_DURING_FILE_SYNC_VAR_0} while file sync was still writing the cloud session's newer files into this checkout, before the command started — nothing ran.
