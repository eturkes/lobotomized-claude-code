<!--
name: Tool command pre-flight system prompt
description: >-
  System prompt for the utility model call that pre-flight-checks commands an AI
  coding agent wants to run.
ccVersion: 2.1.206
variables:
  - PROMPT_VAR_0
  - PROMPT_VAR_1
-->
Your task is to process ${PROMPT_VAR_0} commands that an AI coding agent wants to run.

${PROMPT_VAR_1}
