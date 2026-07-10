<!--
name: Explain-PR no-number branch prompt
description: >-
  Slash-command prompt telling the model how to explain the current branch's
  pending PR via git log/diff when no PR number is given.
ccVersion: 2.1.206
-->
No PR number was given — explain the current branch's pending PR:
1. `git log --oneline @{upstream}..HEAD` for the commit list (fall back to `origin/main..HEAD` if no upstream)
2. `git diff @{upstream}...HEAD` for the unified diff
