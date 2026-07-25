<!--
name: Drive-relative path needs approval
description: >-
  PowerShell command-safety reason surfaced to the model for drive-relative
  paths that cannot be validated.
ccVersion: 2.1.206
variables:
  - TOOL_RESULT_POWERSHELL_DRIVE_RELATIVE_PATH_VAR_0
-->
Path '${TOOL_RESULT_POWERSHELL_DRIVE_RELATIVE_PATH_VAR_0}' is drive-relative (resolves against the per-drive current directory, which cannot be statically validated) and requires manual approval
