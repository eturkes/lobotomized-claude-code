<!--
name: Session worktree isolation guard
description: >-
  Edit/Write validation error returned to the model when an isolated session
  edits a shared-checkout path.
ccVersion: 2.1.206
variables:
  - TOOL_RESULT_SESSION_WORKTREE_ISOLATION_GUARD_VAR_0
  - TOOL_RESULT_SESSION_WORKTREE_ISOLATION_GUARD_VAR_1
  - TOOL_RESULT_SESSION_WORKTREE_ISOLATION_GUARD_VAR_2
  - TOOL_RESULT_SESSION_WORKTREE_ISOLATION_GUARD_VAR_3
-->
This session is now isolated in ${TOOL_RESULT_SESSION_WORKTREE_ISOLATION_GUARD_VAR_0.worktreePath}. Edit the worktree copy of this file instead of the shared-checkout path.
