<!--
name: Background session isolation guard
description: >-
  Edit/Write validation error returned to the model when a background session
  hasn't isolated its changes yet.
ccVersion: 2.1.206
variables:
  - TOOL_RESULT_BG_SESSION_ISOLATION_GUARD_VAR_0
-->
This background session hasn't isolated its changes yet. Call ${TOOL_RESULT_BG_SESSION_ISOLATION_GUARD_VAR_0} first so edits land in a worktree instead of the shared checkout, then retry this edit using the worktree path. (To disable this guard for this repo, set \`"worktree": {"bgIsolation": "none"}\` in .claude/settings.json.)
