<!--
name: Stop-hook condition judge prompt
description: >-
  Prompt for the utility model judging whether a stop-hook condition has been
  satisfied from the transcript.
ccVersion: 2.1.206
variables:
  - AGENT_PROMPT_STOP_HOOK_CONDITION_JUDGE_VAR_0
-->
Based on the conversation transcript above, has the following stopping condition been satisfied? Answer based on transcript evidence only.

Condition: ${AGENT_PROMPT_STOP_HOOK_CONDITION_JUDGE_VAR_0.prompt}
