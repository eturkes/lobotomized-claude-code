<!--
name: Subagent bg-isolation guard
description: >-
  Edit/Write validation error returned to the model when a subagent's parent bg
  session hasn't isolated yet.
ccVersion: 2.1.206
variables:
  - TOOL_RESULT_SUBAGENT_BG_ISOLATION_GUARD_VAR_0
-->
This subagent's parent bg session hasn't isolated yet, so writes to the shared checkout are blocked. Re-spawn this agent with \`isolation: "worktree"\`, or have the parent call ${TOOL_RESULT_SUBAGENT_BG_ISOLATION_GUARD_VAR_0} before spawning. (To disable this guard for this repo, set \`"worktree": {"bgIsolation": "none"}\` in .claude/settings.json.)
