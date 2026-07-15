<!--
name: 'Data: Artifact connected-source guidance'
description: >-
  Directs Artifact authors to load the runtime capabilities skill before
  declaring live connector access; appended to the Artifact skill markdown.
ccVersion: 2.1.210
variables:
  - ARTIFACT_CAPABILITIES_SKILL_NAME
-->


## Live data via connected sources

When the artifact's data lives in one of the user's connected data sources rather than in the conversation, the published page can fetch it live: declare the \`mcp\` capability when publishing, and have the page call the user's connectors at runtime. Load the \`${ARTIFACT_CAPABILITIES_SKILL_NAME}\` skill first for the typed call definitions and manifest rules. Without this capability, build from data available in the conversation as usual.
