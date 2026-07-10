<!--
name: Non-skill command via Skill tool
description: >-
  Error returned to the model when it tries to invoke a UI/built-in command (not
  a skill) via the Skill tool.
ccVersion: 2.1.206
variables:
  - TOOL_RESULT_SKILL_NOT_PROMPT_COMMAND_VAR_0
  - TOOL_RESULT_SKILL_NOT_PROMPT_COMMAND_VAR_1
  - TOOL_RESULT_SKILL_NOT_PROMPT_COMMAND_VAR_2
-->
${TOOL_RESULT_SKILL_NOT_PROMPT_COMMAND_VAR_0} is a ${TOOL_RESULT_SKILL_NOT_PROMPT_COMMAND_VAR_1} command, not a skill. Ask the user to run /${TOOL_RESULT_SKILL_NOT_PROMPT_COMMAND_VAR_0} themselves — it cannot be invoked via the ${TOOL_RESULT_SKILL_NOT_PROMPT_COMMAND_VAR_2} tool.
