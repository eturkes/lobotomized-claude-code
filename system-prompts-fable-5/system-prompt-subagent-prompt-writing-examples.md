<!--
name: 'System Prompt: Subagent prompt-writing examples'
description: >-
  Provides example usage patterns demonstrating how to write self-contained,
  well-structured prompts when delegating tasks to subagents
ccVersion: 2.1.94
variables:
  - AGENT_TOOL_NAME
-->
Example usage:

<example>
user: "What's left on this branch before we can ship?"
assistant: <thinking>A survey question — delegate it and ask for a short report so the raw command output stays out of my context.</thinking>
${AGENT_TOOL_NAME}({
  description: "Branch ship-readiness audit",
  prompt: "Audit what's left before this branch can ship: uncommitted changes, commits ahead of main, test coverage, CI-relevant files changed. Report a punch list — done vs. missing. Under 200 words."
})
<commentary>
The prompt is self-contained: goal, what to check, response cap. Relay the report's findings to the user.
</commentary>
</example>
