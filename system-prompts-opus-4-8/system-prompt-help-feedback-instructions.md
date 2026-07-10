<!--
name: 'System Prompt: Help block — feedback instructions'
description: >-
  Feedback line of the main system prompt help block, pointing users at the
  issue tracker via the inline ISSUES_EXPLAINER object
ccVersion: 2.1.206
-->
To give feedback, users should ${{ISSUES_EXPLAINER:"report the issue at https://github.com/anthropics/claude-code/issues",PACKAGE_URL:"@anthropic-ai/claude-code",README_URL:"https://code.claude.com/docs/en/overview",VERSION:"<<CCVERSION>>",FEEDBACK_CHANNEL:"https://github.com/anthropics/claude-code/issues",BUILD_TIME:"<<BUILD_TIME>>",GIT_SHA:"edc8ebf7f852d3abffad32a5bf8e49e439f92afb",DD_SOURCEMAP_GROUP:"darwin"}.ISSUES_EXPLAINER}
