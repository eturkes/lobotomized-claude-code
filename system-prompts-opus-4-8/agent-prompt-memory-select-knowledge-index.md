<!--
name: Memory select knowledge-index context
description: >-
  Knowledge-index results block injected into the memory-selection utility
  prompt for the model to choose from.
ccVersion: 2.1.206
variables:
  - AGENT_PROMPT_MEMORY_SELECT_KNOWLEDGE_INDEX_VAR_0
  - AGENT_PROMPT_MEMORY_SELECT_KNOWLEDGE_INDEX_VAR_1
-->


Knowledge-index results for this query (select by id):
${AGENT_PROMPT_MEMORY_SELECT_KNOWLEDGE_INDEX_VAR_0(AGENT_PROMPT_MEMORY_SELECT_KNOWLEDGE_INDEX_VAR_1)}
