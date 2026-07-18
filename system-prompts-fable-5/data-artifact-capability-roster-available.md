<!--
name: 'Data: Artifact capability roster available'
description: >-
  Interpolated into the artifact-capabilities skill guidance to enumerate the
  capability names this user may declare
ccVersion: 2.1.214
variables:
  - DATA_ARTIFACT_CAPABILITY_ROSTER_AVAILABLE_VAR_0
  - DATA_ARTIFACT_CAPABILITY_ROSTER_AVAILABLE_VAR_1
-->
**Available capabilities:** ${DATA_ARTIFACT_CAPABILITY_ROSTER_AVAILABLE_VAR_0.map((DATA_ARTIFACT_CAPABILITY_ROSTER_AVAILABLE_VAR_1)=>`\`${DATA_ARTIFACT_CAPABILITY_ROSTER_AVAILABLE_VAR_1}\``).join(", ")} — the complete set you may declare.
