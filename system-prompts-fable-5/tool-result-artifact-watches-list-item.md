<!--
name: 'Tool Result: Artifact watches list item'
description: >-
  Per-watch line in the watches tool result showing url, connection state,
  whether requested or publish-armed, and the since timestamp.
ccVersion: null
variables:
  - TOOL_RESULT_ARTIFACT_WATCHES_LIST_ITEM_VAR_0
  - TOOL_RESULT_ARTIFACT_WATCHES_LIST_ITEM_VAR_1
-->
- ${TOOL_RESULT_ARTIFACT_WATCHES_LIST_ITEM_VAR_0.url} — ${TOOL_RESULT_ARTIFACT_WATCHES_LIST_ITEM_VAR_0.connected?"connected":"reconnecting"}, ${TOOL_RESULT_ARTIFACT_WATCHES_LIST_ITEM_VAR_0.explicit?"requested by you":"armed by a publish"}, since ${new TOOL_RESULT_ARTIFACT_WATCHES_LIST_ITEM_VAR_1(TOOL_RESULT_ARTIFACT_WATCHES_LIST_ITEM_VAR_0.since).toISOString()}
