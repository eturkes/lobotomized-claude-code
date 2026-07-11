<!--
name: ClaudeDesign finalize_plan Scope Unavailable (Subagent/Hook)
description: >-
  Permission-deny message returned to the model when finalize_plan requests
  scope "project" in a subagent/PermissionRequest-hook context.
ccVersion: 2.1.207
-->
ClaudeDesign finalize_plan: scope "project" is not available in this context (plan approvals are not recorded in subagent or PermissionRequest-hook sessions, so a project-wide grant has no effect) — use the classic per-batch flow (writes/deletes without scope).
