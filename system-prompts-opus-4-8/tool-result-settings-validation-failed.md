<!--
name: settings.json validation failed after edit
description: >-
  Tool result returned to the model when an edit to settings.json fails schema
  validation, including the schema and a do-not-touch-env instruction.
ccVersion: 2.1.206
variables:
  - TOOL_RESULT_SETTINGS_VALIDATION_FAILED_VAR_0
-->
Claude Code settings.json validation failed after edit:
${TOOL_RESULT_SETTINGS_VALIDATION_FAILED_VAR_0.error}

Full schema:
${TOOL_RESULT_SETTINGS_VALIDATION_FAILED_VAR_0.fullSchema}
IMPORTANT: Do not update the env unless explicitly instructed to do so.
