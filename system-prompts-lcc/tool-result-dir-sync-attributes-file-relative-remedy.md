<!--
name: 'Dir-sync: attributes-file relative-path remedy'
description: >-
  Explains that dir-sync cannot follow a relative attributes-file setting here,
  and offers moving its rules into a committed .gitattributes file or setting it
  only in the user's own gitconfig.
ccVersion: 2.1.284
variables:
  - TOOL_RESULT_DIR_SYNC_ATTRIBUTES_FILE_RELATIVE_REMEDY_VAR_0
-->
sync cannot follow ${TOOL_RESULT_DIR_SYNC_ATTRIBUTES_FILE_RELATIVE_REMEDY_VAR_0} here; move its rules into a committed .gitattributes file and delete the setting, or set it only in your ~/.gitconfig, to an absolute or ~/ path
