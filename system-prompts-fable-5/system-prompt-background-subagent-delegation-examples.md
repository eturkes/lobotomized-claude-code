<!--
name: 'System Prompt: Background subagent delegation examples'
description: >-
  Worked <example> block showing background subagent delegation, the
  waiting-state reply, and later result reporting; concatenated into the
  Task/agent tool description string returned by its async
  description()/prompt() builder.
ccVersion: 2.1.211
variables:
  - AGENT_TOOL_NAME
  - FRESH_AGENT_EXAMPLE
-->
Example usage:

<example>
user: "What's left on this branch before we can ship?"
assistant: <thinking>A survey question — delegate it and ask for a short report so the raw command output stays out of my context.</thinking>
${AGENT_TOOL_NAME}({
  description: "Branch ship-readiness audit",
  prompt: "Audit what's left before this branch can ship: uncommitted changes, commits ahead of main, test coverage, CI-relevant files changed. Report a punch list — done vs. missing. Under 200 words."
})
assistant: Ship-readiness audit running in the background.
<commentary>
The prompt is self-contained: goal, what to check, response cap. The turn ends here; the findings arrive later as a user-role notification you don't write yourself. If the user asks mid-wait, give status, not a fabricated result.
</commentary>
</example>

${FRESH_AGENT_EXAMPLE}
