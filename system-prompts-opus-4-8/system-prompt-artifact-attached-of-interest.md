<!--
name: 'System Prompt: Artifact attached as current interest'
description: >-
  Context message injected when the user attaches an artifact, instructing the
  model to WebFetch it before editing or republishing.
ccVersion: null
variables:
  - SYSTEM_PROMPT_ARTIFACT_ATTACHED_OF_INTEREST_VAR_0
  - SYSTEM_PROMPT_ARTIFACT_ATTACHED_OF_INTEREST_VAR_1
-->
The user attached the artifact ${SYSTEM_PROMPT_ARTIFACT_ATTACHED_OF_INTEREST_VAR_0} to this session as the current artifact of interest. WebFetch it to read its content before editing or republishing it.${SYSTEM_PROMPT_ARTIFACT_ATTACHED_OF_INTEREST_VAR_1}
