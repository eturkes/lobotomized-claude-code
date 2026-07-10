<!--
name: Artifact connector-merge warning
description: >-
  Publish-manifest warning returned to the model when multiple manifest entries
  resolve to one connector and are merged.
ccVersion: 2.1.206
variables:
  - TOOL_RESULT_ARTIFACT_MANIFEST_CONNECTOR_MERGE_WARNING_VAR_0
  - TOOL_RESULT_ARTIFACT_MANIFEST_CONNECTOR_MERGE_WARNING_VAR_1
  - TOOL_RESULT_ARTIFACT_MANIFEST_CONNECTOR_MERGE_WARNING_VAR_2
  - TOOL_RESULT_ARTIFACT_MANIFEST_CONNECTOR_MERGE_WARNING_VAR_3
-->
${TOOL_RESULT_ARTIFACT_MANIFEST_CONNECTOR_MERGE_WARNING_VAR_0.from} manifest entries resolve to connector "${TOOL_RESULT_ARTIFACT_MANIFEST_CONNECTOR_MERGE_WARNING_VAR_1}" and were merged into one (${TOOL_RESULT_ARTIFACT_MANIFEST_CONNECTOR_MERGE_WARNING_VAR_2} ${TOOL_RESULT_ARTIFACT_MANIFEST_CONNECTOR_MERGE_WARNING_VAR_3(TOOL_RESULT_ARTIFACT_MANIFEST_CONNECTOR_MERGE_WARNING_VAR_2,"tool")}). A viewer with more than one connector named "${TOOL_RESULT_ARTIFACT_MANIFEST_CONNECTOR_MERGE_WARNING_VAR_1}" gets server_ambiguous on every call until the duplicates are renamed or removed.
