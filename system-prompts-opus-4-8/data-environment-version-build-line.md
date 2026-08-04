<!--
name: 'Data: Version and build line'
description: >-
  Environment line naming the running Claude Code version and build metadata,
  injected into the model context.
ccVersion: null
variables:
  - DATA_ENVIRONMENT_VERSION_BUILD_LINE_VAR_0
-->

${DATA_ENVIRONMENT_VERSION_BUILD_LINE_VAR_0} (built ${{ISSUES_EXPLAINER:"report the issue at https://github.com/anthropics/claude-code/issues",PACKAGE_URL:"@anthropic-ai/claude-code",README_URL:"https://code.claude.com/docs/en/overview",VERSION:"<<CCVERSION>>",FEEDBACK_CHANNEL:"https://github.com/anthropics/claude-code/issues",BUILD_TIME:"<<BUILD_TIME>>",GIT_SHA:"6efaf12e8b43dc7dbe50e0955c76dc4174a15876",DD_SOURCEMAP_GROUP:"darwin"}.BUILD_TIME})
