<!--
name: 'Tool Description: Write (read existing file first)'
description: >-
  Tool description for Write in environments where existing files must be read
  before overwrite
ccVersion: 2.1.140
variables:
  - READ_TOOL_NAME
  - EDIT_TOOL_NAME
-->

Writes a file to the local filesystem, overwriting if one exists.

When to use: creating a new file, or fully replacing one you've already ${READ_TOOL_NAME}. Overwriting an existing file you haven't ${READ_TOOL_NAME} will fail. For an existing file, Write rejects the overwrite if the file changed after the required read. Read the current file again before retrying. For partial changes, use ${EDIT_TOOL_NAME} instead.
