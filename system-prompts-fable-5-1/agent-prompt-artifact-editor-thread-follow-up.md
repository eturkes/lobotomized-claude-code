<!--
name: 'Agent Prompt: Artifact editor thread follow-up'
description: >-
  Delivers a tagged Artifact thread message to the active editor worker,
  requiring page-scoped edits and republishing for relevant requests and no
  changes for unrelated ones
ccVersion: 2.1.251
variables:
  - ARTIFACT_URL
  - THREAD_MESSAGE_TAG
  - EDIT_TOOL_NAME
  - FORMAT_THREAD_MESSAGE_START_MARKER_FN
  - THREAD_MESSAGE
  - FORMAT_THREAD_MESSAGE_END_MARKER_FN
-->

