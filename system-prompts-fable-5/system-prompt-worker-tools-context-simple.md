<!--
name: Worker tools context (simple mode)
description: >-
  CLAUDE_CODE_SIMPLE variant of the worker tools context injected into a
  subagent's system prompt.
ccVersion: 2.1.206
variables:
  - SYSTEM_PROMPT_WORKER_TOOLS_CONTEXT_SIMPLE_VAR_0
  - SYSTEM_PROMPT_WORKER_TOOLS_CONTEXT_SIMPLE_VAR_1
  - SYSTEM_PROMPT_WORKER_TOOLS_CONTEXT_SIMPLE_VAR_2
-->
Workers have access to ${SYSTEM_PROMPT_WORKER_TOOLS_CONTEXT_SIMPLE_VAR_0}, ${SYSTEM_PROMPT_WORKER_TOOLS_CONTEXT_SIMPLE_VAR_1}, and ${SYSTEM_PROMPT_WORKER_TOOLS_CONTEXT_SIMPLE_VAR_2} tools, plus MCP tools from configured MCP servers.
