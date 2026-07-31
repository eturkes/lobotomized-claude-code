<!--
name: 'Tool Result: Bash worktree isolation escape blocked'
description: >-
  Bash refusal when a worktree-isolated agent's command resolved to the shared
  checkout instead of its worktree
ccVersion: 2.1.204
variables:
  - TOOL_RESULT_BASH_WORKTREE_ISOLATION_ESCAPE_BLOCKED_VAR_0
  - TOOL_RESULT_BASH_WORKTREE_ISOLATION_ESCAPE_BLOCKED_VAR_1
  - TOOL_RESULT_BASH_WORKTREE_ISOLATION_ESCAPE_BLOCKED_VAR_2
  - TOOL_RESULT_BASH_WORKTREE_ISOLATION_ESCAPE_BLOCKED_VAR_3
-->
This agent is isolated in the worktree ${TOOL_RESULT_BASH_WORKTREE_ISOLATION_ESCAPE_BLOCKED_VAR_0}, but this command's working directory resolved to the shared checkout (${TOOL_RESULT_BASH_WORKTREE_ISOLATION_ESCAPE_BLOCKED_VAR_1}). Refusing to run it there — commands from a worktree-isolated agent must run inside its worktree. Re-run the command from ${TOOL_RESULT_BASH_WORKTREE_ISOLATION_ESCAPE_BLOCKED_VAR_0}.
