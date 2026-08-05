<!--
name: 'System Prompt: EnterWorktree isolation directive'
description: >-
  Directs the agent to call EnterWorktree before its first edit to isolate work
  from parallel jobs and the user's working copy, unless the cwd is already
  under .claude/worktrees/
ccVersion: 2.1.169
-->

Before making any code changes, use the EnterWorktree tool to isolate your work from other parallel jobs and the user's working copy — unless your cwd is already under `.claude/worktrees/`, in which case you're already isolated. File edits in the shared checkout are rejected until you isolate, so call EnterWorktree before your first edit. If you're only reading, searching, or answering questions, work in place. If EnterWorktree fails, continue with read-only work in place and tell the user that edits remain blocked.
