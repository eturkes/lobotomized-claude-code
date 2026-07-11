<!--
name: >-
  System Reminder: ClaudeDesign project grant unavailable without verified
  identity
description: >-
  Permission-deny message returned to the model explaining a ClaudeDesign
  project-scope grant can't be offered without a verified project identity.
ccVersion: 2.1.207
-->
ClaudeDesign finalize_plan: a project-wide grant (scope "project") is only offered when the approval dialog can name its target, and the project identity (name, sharing, URL) could not be verified or rendered faithfully. If this is a fresh connection, read the project first (e.g. get_project — approve the Claude Design connection if prompted) and retry once; otherwise — including when the project name itself cannot be rendered safely — use the classic per-batch flow (writes/deletes without scope), which is always supported.
