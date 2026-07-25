<!--
name: 'Data: Artifact window.claude contract unavailable'
description: >-
  Skill call-contract fallback text injected when the served window.claude type
  definitions could not be extracted, warning the model not to write mcp calls
  from memory.
ccVersion: 2.1.210
variables:
  - DATA_ARTIFACT_WINDOW_CLAUDE_CONTRACT_UNAVAILABLE_VAR_0
-->
**Call contract.** The served \`window.claude\` type definitions could not be extracted for this invocation — invoking this skill again retries. Do not write \`window.claude.mcp\` calls from memory; the served definitions are the authority. ${DATA_ARTIFACT_WINDOW_CLAUDE_CONTRACT_UNAVAILABLE_VAR_0}
