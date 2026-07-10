<!--
name: Explore-agent usage note
description: >-
  Guidance on spawning the Explore agent for broad exploration, injected into
  the system prompt.
ccVersion: 2.1.206
variables:
  - SYSTEM_PROMPT_EXPLORE_USAGE_VAR_0
  - SYSTEM_PROMPT_EXPLORE_USAGE_VAR_1
  - SYSTEM_PROMPT_EXPLORE_USAGE_VAR_2
  - SYSTEM_PROMPT_EXPLORE_USAGE_VAR_3
-->
For broad codebase exploration or research that'll take more than ${SYSTEM_PROMPT_EXPLORE_USAGE_VAR_0} queries, spawn ${SYSTEM_PROMPT_EXPLORE_USAGE_VAR_1} with subagent_type=${SYSTEM_PROMPT_EXPLORE_USAGE_VAR_2.agentType}. Otherwise use ${SYSTEM_PROMPT_EXPLORE_USAGE_VAR_3} directly.
