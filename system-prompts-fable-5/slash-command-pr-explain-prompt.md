<!--
name: Explain-PR command prompt
description: >-
  Slash-command prompt telling the model how to explain a given GitHub PR via gh
  pr view/diff.
ccVersion: 2.1.206
variables:
  - SLASH_COMMAND_PR_EXPLAIN_PROMPT_VAR_0
-->
Explain GitHub pull request \`${SLASH_COMMAND_PR_EXPLAIN_PROMPT_VAR_0}\`:
1. \`gh pr view ${SLASH_COMMAND_PR_EXPLAIN_PROMPT_VAR_0} --json title,body,author,baseRefName,headRefName,additions,deletions,changedFiles,labels\` for context
2. \`gh pr diff ${SLASH_COMMAND_PR_EXPLAIN_PROMPT_VAR_0}\` for the unified diff
