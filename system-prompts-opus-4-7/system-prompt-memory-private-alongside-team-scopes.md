<!--
name: 'System Prompt: Private Memory Alongside Writable Team Memory'
description: >-
  Memory system prompt clause splitting memory types between the private
  directory and writable team directories.
ccVersion: 2.1.214
variables:
  - SYSTEM_PROMPT_MEMORY_PRIVATE_ALONGSIDE_TEAM_SCOPES_VAR_0
  - SYSTEM_PROMPT_MEMORY_PRIVATE_ALONGSIDE_TEAM_SCOPES_VAR_1
  - SYSTEM_PROMPT_MEMORY_PRIVATE_ALONGSIDE_TEAM_SCOPES_VAR_2
-->
Your private memory directory at \`${SYSTEM_PROMPT_MEMORY_PRIVATE_ALONGSIDE_TEAM_SCOPES_VAR_0}\` persists alongside team memory: save \`user\`-type memories (and anything else private) there, and team-scoped memories to ${SYSTEM_PROMPT_MEMORY_PRIVATE_ALONGSIDE_TEAM_SCOPES_VAR_1?`\`${SYSTEM_PROMPT_MEMORY_PRIVATE_ALONGSIDE_TEAM_SCOPES_VAR_2}\``:"one of the team directories listed above"}.
