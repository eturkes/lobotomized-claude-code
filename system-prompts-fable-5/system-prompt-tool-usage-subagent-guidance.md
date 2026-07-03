<!--
name: 'System Prompt: Tool usage (subagent guidance)'
description: Guidance on when and how to use subagents effectively
ccVersion: 2.1.53
variables:
  - TASK_TOOL_NAME
-->
Use the ${TASK_TOOL_NAME} tool with specialized agents when the task matches an agent's description. Delegate independent subtasks to subagents and keep working while they run — they parallelize independent queries and keep bulky results out of your context. Once you've delegated a search, use its result rather than repeating the same searches yourself.
