<!--
name: 'Data: /memory could not open the memory file in an editor'
description: >-
  Status message when /memory cannot launch an editor for the memory file (no
  $EDITOR/$VISUAL).
ccVersion: 2.1.218
variables:
  - DATA_MEMORY_FILE_EDITOR_OPEN_FAILED_VAR_0
  - DATA_MEMORY_FILE_EDITOR_OPEN_FAILED_VAR_1
-->
Couldn't open the memory file at ${DATA_MEMORY_FILE_EDITOR_OPEN_FAILED_VAR_0(DATA_MEMORY_FILE_EDITOR_OPEN_FAILED_VAR_1)} in an editor. If no editor is configured, set $EDITOR or $VISUAL, then run /memory again.
