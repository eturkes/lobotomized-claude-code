<!--
name: Agentic session search prompt
description: >-
  Prompt sent to a utility model to grep transcript .jsonl files under scoped
  directories and find sessions matching a search query.
ccVersion: 2.1.206
variables:
  - SYSTEM_PROMPT_AGENTIC_SESSION_SEARCH_VAR_0
  - SYSTEM_PROMPT_AGENTIC_SESSION_SEARCH_VAR_1
  - SYSTEM_PROMPT_AGENTIC_SESSION_SEARCH_VAR_2
-->
Search query: "${SYSTEM_PROMPT_AGENTIC_SESSION_SEARCH_VAR_0}"

Search ONLY these transcript directories (other paths are out of scope):
${SYSTEM_PROMPT_AGENTIC_SESSION_SEARCH_VAR_1.join(`
`)}

Recent sessions (id title metadata) — partial list, the match may not be here:
${SYSTEM_PROMPT_AGENTIC_SESSION_SEARCH_VAR_2}

Find sessions whose transcript content matches the query by grepping the .jsonl files under the directories above.
