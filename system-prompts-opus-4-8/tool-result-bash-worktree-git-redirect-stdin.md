<!--
name: 'Tool Result: Worktree git args from stdin'
description: >-
  Deny-reason fragment when a worktree-isolated git command takes its arguments
  from stdin (xargs/parallel), making its target repo unverifiable.
ccVersion: null
-->
feeds git its arguments from stdin at runtime (xargs/parallel), so the repository it targets cannot be verified
