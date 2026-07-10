<!--
name: 'Memory: private and team directories'
description: >-
  Memory system prompt line naming the private and team directories; injected
  into model context.
ccVersion: 2.1.206
variables:
  - SYSTEM_PROMPT_MEMORY_DIRECTORIES_PRIVATE_TEAM_VAR_0
  - SYSTEM_PROMPT_MEMORY_DIRECTORIES_PRIVATE_TEAM_VAR_1
  - SYSTEM_PROMPT_MEMORY_DIRECTORIES_PRIVATE_TEAM_VAR_2
-->
at \`${SYSTEM_PROMPT_MEMORY_DIRECTORIES_PRIVATE_TEAM_VAR_0}\` (private to this user) and \`${SYSTEM_PROMPT_MEMORY_DIRECTORIES_PRIVATE_TEAM_VAR_1}\` (shared with all users of this project). ${SYSTEM_PROMPT_MEMORY_DIRECTORIES_PRIVATE_TEAM_VAR_2}
