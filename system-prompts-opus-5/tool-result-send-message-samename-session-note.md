<!--
name: Same-named session note
description: >-
  Note appended to the SendMessage model tool result about other same-named
  sessions.
ccVersion: 2.1.206
variables:
  - TOOL_RESULT_SEND_MESSAGE_SAMENAME_SESSION_NOTE_VAR_0
-->

Note: ${TOOL_RESULT_SEND_MESSAGE_SAMENAME_SESSION_NOTE_VAR_0.sameNamedSiblings} other live session${TOOL_RESULT_SEND_MESSAGE_SAMENAME_SESSION_NOTE_VAR_0.sameNamedSiblings===1?" is":"s are"} also named '${TOOL_RESULT_SEND_MESSAGE_SAMENAME_SESSION_NOTE_VAR_0.displayName}'. This went to the one this conversation confirmed; to switch, re-send with that session's 'name [ref]'.
