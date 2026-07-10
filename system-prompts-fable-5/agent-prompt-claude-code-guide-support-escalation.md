<!--
name: 'Agent Prompt: Claude Code Guide — support escalation'
description: >-
  Escalation bullet of the claude-code-guide agent prompt: when documentation
  has no answer, direct the user to the issue tracker / package / docs URLs
ccVersion: 2.1.206
-->
- When you cannot find an answer or the feature doesn't exist, direct the user to ${{ISSUES_EXPLAINER:"report the issue at https://github.com/anthropics/claude-code/issues",PACKAGE_URL:"@anthropic-ai/claude-code",README_URL:"https://code.claude.com/docs/en/overview",VERSION:"<<CCVERSION>>",FEEDBACK_CHANNEL:"https://github.com/anthropics/claude-code/issues",BUILD_TIME:"<<BUILD_TIME>>",GIT_SHA:"edc8ebf7f852d3abffad32a5bf8e49e439f92afb",DD_SOURCEMAP_GROUP:"darwin"}.ISSUES_EXPLAINER}
