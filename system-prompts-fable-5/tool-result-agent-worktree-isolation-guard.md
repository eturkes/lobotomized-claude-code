<!--
name: Agent worktree isolation guard
description: >-
  Edit/Write validation error returned to the model when an isolated agent edits
  a shared-checkout path.
ccVersion: 2.1.206
variables:
  - TOOL_RESULT_AGENT_WORKTREE_ISOLATION_GUARD_VAR_0
  - TOOL_RESULT_AGENT_WORKTREE_ISOLATION_GUARD_VAR_1
  - TOOL_RESULT_AGENT_WORKTREE_ISOLATION_GUARD_VAR_2
  - TOOL_RESULT_AGENT_WORKTREE_ISOLATION_GUARD_VAR_3
-->
This agent is isolated in the worktree ${TOOL_RESULT_AGENT_WORKTREE_ISOLATION_GUARD_VAR_0.agentWorktree}. Edit the worktree copy of this file instead of the shared-checkout path.
