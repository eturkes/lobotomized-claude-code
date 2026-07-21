<!--
name: 'Tool Result: Worktree-isolated git redirect blocked'
description: >-
  Bash-tool refusal returned to the model when a worktree-isolated agent's
  command would redirect git into the shared checkout.
ccVersion: null
variables:
  - TOOL_RESULT_WORKTREE_ISOLATED_GIT_REDIRECT_BLOCKED_VAR_0
  - TOOL_RESULT_WORKTREE_ISOLATED_GIT_REDIRECT_BLOCKED_VAR_1
-->
This agent is isolated in the worktree ${TOOL_RESULT_WORKTREE_ISOLATED_GIT_REDIRECT_BLOCKED_VAR_0}, but this command ${TOOL_RESULT_WORKTREE_ISOLATED_GIT_REDIRECT_BLOCKED_VAR_1}. Refusing to run it — a worktree-isolated agent's git operations must target its own worktree. Run the equivalent from ${TOOL_RESULT_WORKTREE_ISOLATED_GIT_REDIRECT_BLOCKED_VAR_0} without the redirect.
