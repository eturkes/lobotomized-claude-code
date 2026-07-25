<!--
name: Command-failed message
description: >-
  User-turn content injected into the model conversation reporting a failed
  local command.
ccVersion: 2.1.206
variables:
  - PROMPT_VAR_0
  - PROMPT_VAR_1
  - PROMPT_VAR_2
  - PROMPT_VAR_3
-->
<${PROMPT_VAR_0}>Command failed: ${PROMPT_VAR_1(PROMPT_VAR_2(PROMPT_VAR_3))}</${PROMPT_VAR_0}>
