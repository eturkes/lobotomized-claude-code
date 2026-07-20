<!--
name: 'Slash Command: /import --yes Nothing To Confirm'
description: >-
  Output of `/import --yes` when no prior preview exists; returned as
  {type:'text'} and wrapped in <local-command-stdout>, which tN() replays to the
  model as a user message.
ccVersion: 2.1.214
variables:
  - SLASH_COMMAND_IMPORT_YES_NOTHING_TO_CONFIRM_VAR_0
-->
Nothing to confirm: run \`${SLASH_COMMAND_IMPORT_YES_NOTHING_TO_CONFIRM_VAR_0}\` first (without --yes) in this same session to see what will be imported, then \`${SLASH_COMMAND_IMPORT_YES_NOTHING_TO_CONFIRM_VAR_0} --yes\`. On plain \`claude -p\`, where each invocation is a separate process, use \`claude import\` from a terminal instead.
