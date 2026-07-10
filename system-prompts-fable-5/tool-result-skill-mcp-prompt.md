<!--
name: MCP prompt via Skill tool
description: >-
  Error returned to the model when it tries to invoke an MCP prompt (not a
  skill) via the Skill tool.
ccVersion: 2.1.206
variables:
  - TOOL_RESULT_SKILL_MCP_PROMPT_VAR_0
  - TOOL_RESULT_SKILL_MCP_PROMPT_VAR_1
-->
${TOOL_RESULT_SKILL_MCP_PROMPT_VAR_0} is an MCP prompt, not a skill. Ask the user to run /${TOOL_RESULT_SKILL_MCP_PROMPT_VAR_0} themselves — it cannot be invoked via the ${TOOL_RESULT_SKILL_MCP_PROMPT_VAR_1} tool.
