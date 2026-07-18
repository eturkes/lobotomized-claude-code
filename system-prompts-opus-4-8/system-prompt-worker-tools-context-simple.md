<!--
name: 'System Prompt: Worker Tools Context (simple)'
description: >-
  CLAUDE_CODE_SIMPLE branch of getCoordinatorSystemPrompt(), interpolated into
  the coordinator-mode system prompt to tell the coordinator which tools its
  workers have.
ccVersion: 2.1.214
variables:
  - SYSTEM_PROMPT_WORKER_TOOLS_CONTEXT_SIMPLE_VAR_0
  - SYSTEM_PROMPT_WORKER_TOOLS_CONTEXT_SIMPLE_VAR_1
  - SYSTEM_PROMPT_WORKER_TOOLS_CONTEXT_SIMPLE_VAR_2
  - SYSTEM_PROMPT_WORKER_TOOLS_CONTEXT_SIMPLE_VAR_3
-->
Workers have access to ${SYSTEM_PROMPT_WORKER_TOOLS_CONTEXT_SIMPLE_VAR_0}, ${SYSTEM_PROMPT_WORKER_TOOLS_CONTEXT_SIMPLE_VAR_1}, ${SYSTEM_PROMPT_WORKER_TOOLS_CONTEXT_SIMPLE_VAR_2}, and ${SYSTEM_PROMPT_WORKER_TOOLS_CONTEXT_SIMPLE_VAR_3} tools, plus MCP tools from configured MCP servers. Workers can fan out further via ${SYSTEM_PROMPT_WORKER_TOOLS_CONTEXT_SIMPLE_VAR_3}.
