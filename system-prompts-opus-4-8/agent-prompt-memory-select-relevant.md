<!--
name: Memory select-relevant prompt
description: >-
  Prompt for the memory-selection utility model asking it to select memories
  relevant to a query.
ccVersion: 2.1.206
variables:
  - AGENT_PROMPT_MEMORY_SELECT_RELEVANT_VAR_0
  - AGENT_PROMPT_MEMORY_SELECT_RELEVANT_VAR_1
-->
Select memories relevant to:
${AGENT_PROMPT_MEMORY_SELECT_RELEVANT_VAR_0}

(${AGENT_PROMPT_MEMORY_SELECT_RELEVANT_VAR_1.length} knowledge-index results were offered for this query)
