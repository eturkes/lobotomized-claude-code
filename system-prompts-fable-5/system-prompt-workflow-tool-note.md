<!--
name: Workflow tool note in worker context
description: >-
  Workflow-tool bullet in the subagent tools context injected into a worker's
  system prompt.
ccVersion: 2.1.206
variables:
  - SYSTEM_PROMPT_WORKFLOW_TOOL_NOTE_VAR_0
  - SYSTEM_PROMPT_WORKFLOW_TOOL_NOTE_VAR_1
-->
- **${SYSTEM_PROMPT_WORKFLOW_TOOL_NOTE_VAR_0}** (if available) - Run a multi-step subagent pipeline; prefer it over hand-orchestrating ${SYSTEM_PROMPT_WORKFLOW_TOOL_NOTE_VAR_1} calls when a matching workflow exists
