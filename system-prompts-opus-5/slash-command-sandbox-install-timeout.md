<!--
name: 'Slash Command: /sandbox install Timed Out'
description: >-
  Result message of `/sandbox install` on Windows UAC timeout; the local-jsx
  onDone is called without display:'system', so it becomes a
  <local-command-stdout> user message in the model's context.
ccVersion: 2.1.214
variables:
  - SLASH_COMMAND_SANDBOX_INSTALL_TIMEOUT_VAR_0
-->
The install timed out after 60 seconds: ${SLASH_COMMAND_SANDBOX_INSTALL_TIMEOUT_VAR_0}. If an elevation prompt was showing, run /sandbox install again and respond within a minute. If no prompt appeared, the installer may be blocked on this machine — run /sandbox to check sandbox status.
