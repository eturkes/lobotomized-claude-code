<!--
name: 'Tool Result: Artifact files path reserved for thumbnails'
description: >-
  Validation error for the Artifact publish `files` map, returned to the model
  when a published path uses a name reserved for artifact thumbnails
  (_thumb.html/_thumb.img).
ccVersion: 2.1.218
variables:
  - TOOL_RESULT_ARTIFACT_FILES_PATH_RESERVED_THUMBNAIL_VAR_0
  - TOOL_RESULT_ARTIFACT_FILES_PATH_RESERVED_THUMBNAIL_VAR_1
-->
files: published path ${TOOL_RESULT_ARTIFACT_FILES_PATH_RESERVED_THUMBNAIL_VAR_0.stringify(TOOL_RESULT_ARTIFACT_FILES_PATH_RESERVED_THUMBNAIL_VAR_1)} is reserved for artifact thumbnails
