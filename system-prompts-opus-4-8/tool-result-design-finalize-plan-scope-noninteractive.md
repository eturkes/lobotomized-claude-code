<!--
name: ClaudeDesign finalize_plan Scope Denied (Non-Interactive)
description: >-
  Permission-deny message returned to the model when finalize_plan requests
  scope "project" in a non-interactive session.
ccVersion: 2.1.207
-->
ClaudeDesign finalize_plan: scope "project" is not available in non-interactive sessions (plan approvals are not recorded there, so a project-wide grant has no effect) — use the classic per-batch flow (writes/deletes without scope).
