<!--
name: 'Slash Command: /ultrareview Launch Confirmation'
description: >-
  Confirmation text emitted when /ultrareview launches a cloud review session;
  injected into the conversation as a local-command-stdout user message
  alongside a meta follow-up instruction.
ccVersion: 2.1.218
variables:
  - SLASH_COMMAND_ULTRAREVIEW_LAUNCHED_VAR_0
  - SLASH_COMMAND_ULTRAREVIEW_LAUNCHED_VAR_1
  - SLASH_COMMAND_ULTRAREVIEW_LAUNCHED_VAR_2
  - SLASH_COMMAND_ULTRAREVIEW_LAUNCHED_VAR_3
  - SLASH_COMMAND_ULTRAREVIEW_LAUNCHED_VAR_4
  - SLASH_COMMAND_ULTRAREVIEW_LAUNCHED_VAR_5
-->
${SLASH_COMMAND_ULTRAREVIEW_LAUNCHED_VAR_0}Ultrareview launched for ${SLASH_COMMAND_ULTRAREVIEW_LAUNCHED_VAR_1} (${SLASH_COMMAND_ULTRAREVIEW_LAUNCHED_VAR_2()}, runs in the cloud). Track: ${SLASH_COMMAND_ULTRAREVIEW_LAUNCHED_VAR_3}${SLASH_COMMAND_ULTRAREVIEW_LAUNCHED_VAR_4}${SLASH_COMMAND_ULTRAREVIEW_LAUNCHED_VAR_5}
