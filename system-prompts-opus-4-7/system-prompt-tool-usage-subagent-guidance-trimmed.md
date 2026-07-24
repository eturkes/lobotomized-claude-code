<!--
name: 'System Prompt: Tool usage subagent guidance (steered/trimmed)'
description: >-
  Trimmed variant of the tool-usage subagent guidance emitted when the
  subagent-steer experiment is not on 'default': use the Agent tool when the
  task matches an agent's description and never duplicate work a subagent is
  already doing.
ccVersion: 2.1.215
variables:
  - SYSTEM_PROMPT_TOOL_USAGE_SUBAGENT_GUIDANCE_TRIMMED_VAR_0
-->
Use the ${SYSTEM_PROMPT_TOOL_USAGE_SUBAGENT_GUIDANCE_TRIMMED_VAR_0} tool with specialized agents when the task at hand matches the agent's description. Importantly, avoid duplicating work that subagents are already doing - if you delegate research to a subagent, do not also perform the same searches yourself.
