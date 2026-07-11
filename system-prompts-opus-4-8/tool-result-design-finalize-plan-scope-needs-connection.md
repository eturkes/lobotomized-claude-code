<!--
name: ClaudeDesign finalize_plan Scope Needs Connection Approval
description: >-
  Permission-deny message returned to the model when a project-wide
  finalize_plan grant is requested before the Claude Design connection is
  approved.
ccVersion: 2.1.207
-->
ClaudeDesign finalize_plan: a project-wide grant (scope "project") requires the Claude Design connection to be approved first. Read the project (e.g. get_project — approve the connection when prompted), then retry; or use the classic per-batch flow (writes/deletes without scope).
