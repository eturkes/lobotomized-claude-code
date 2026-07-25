<!--
name: 'Tool Result: Subagent Spawn Limit Reached'
description: >-
  AgentPreconditionError message thrown by the Task tool at the spawn cap;
  runToolUse wraps it as <tool_use_error> tool_result content returned to the
  model.
ccVersion: 2.1.214
variables:
  - TOOL_RESULT_TASK_SUBAGENT_SPAWN_LIMIT_VAR_0
  - TOOL_RESULT_TASK_SUBAGENT_SPAWN_LIMIT_VAR_1
-->
Subagent spawn limit reached (${TOOL_RESULT_TASK_SUBAGENT_SPAWN_LIMIT_VAR_0} of ${TOOL_RESULT_TASK_SUBAGENT_SPAWN_LIMIT_VAR_1} agents spawned). Complete the remaining work directly with your tools. Ask the user to raise CLAUDE_CODE_MAX_SUBAGENTS_PER_SESSION if more agents are needed.
