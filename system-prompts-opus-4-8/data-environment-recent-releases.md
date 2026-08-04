<!--
name: 'Data: Recent releases block'
description: >-
  Environment block listing the last ten Claude Code releases and the running
  version, injected into the model context.
ccVersion: null
variables:
  - DATA_ENVIRONMENT_RECENT_RELEASES_VAR_0
-->

**Recent releases (you are running v${{ISSUES_EXPLAINER:"report the issue at https://github.com/anthropics/claude-code/issues",PACKAGE_URL:"@anthropic-ai/claude-code",README_URL:"https://code.claude.com/docs/en/overview",VERSION:"<<CCVERSION>>",FEEDBACK_CHANNEL:"https://github.com/anthropics/claude-code/issues",BUILD_TIME:"<<BUILD_TIME>>",GIT_SHA:"6efaf12e8b43dc7dbe50e0955c76dc4174a15876",DD_SOURCEMAP_GROUP:"darwin"}.VERSION}):**
${DATA_ENVIRONMENT_RECENT_RELEASES_VAR_0.join(`

`)}
