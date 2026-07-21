<!--
name: 'Tool Result: Artifact files path has illegal URL characters'
description: >-
  Validation error for the Artifact publish `files` map, returned to the model
  when a published path contains characters (?, #, %) that can't appear in a
  served URL path.
ccVersion: null
variables:
  - TOOL_RESULT_ARTIFACT_FILES_PATH_ILLEGAL_URL_CHARS_VAR_0
  - TOOL_RESULT_ARTIFACT_FILES_PATH_ILLEGAL_URL_CHARS_VAR_1
-->
files: published path ${TOOL_RESULT_ARTIFACT_FILES_PATH_ILLEGAL_URL_CHARS_VAR_0.stringify(TOOL_RESULT_ARTIFACT_FILES_PATH_ILLEGAL_URL_CHARS_VAR_1)} contains characters that cannot appear in a served URL path ("?", "#", "%")
