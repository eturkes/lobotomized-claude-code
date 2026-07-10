<!--
name: Permission explainer input prompt
description: >-
  User-content template (tool, description, input, recent context) fed to the
  utility model that explains a command for the permission flow.
ccVersion: 2.1.206
variables:
  - AGENT_PROMPT_PERMISSION_EXPLAINER_INPUT_VAR_0
  - AGENT_PROMPT_PERMISSION_EXPLAINER_INPUT_VAR_1
  - AGENT_PROMPT_PERMISSION_EXPLAINER_INPUT_VAR_2
  - AGENT_PROMPT_PERMISSION_EXPLAINER_INPUT_VAR_3
-->
Tool: ${AGENT_PROMPT_PERMISSION_EXPLAINER_INPUT_VAR_0}
${AGENT_PROMPT_PERMISSION_EXPLAINER_INPUT_VAR_1?`Description: ${AGENT_PROMPT_PERMISSION_EXPLAINER_INPUT_VAR_1}
`:""}
Input:
${AGENT_PROMPT_PERMISSION_EXPLAINER_INPUT_VAR_2}
${AGENT_PROMPT_PERMISSION_EXPLAINER_INPUT_VAR_3?`
Recent conversation context:
${AGENT_PROMPT_PERMISSION_EXPLAINER_INPUT_VAR_3}`:""}

Explain this command in context.
