<!--
name: PR Walkthrough Artifact Command Prompt
description: >-
  getPromptForCommand {type:'text',text:WOf(e)} body for the
  shareable-PR-walkthrough slash command, instructing the model to produce a
  self-contained HTML PR walkthrough page and publish it via the artifact tool.
ccVersion: 2.1.206
variables:
  - SYSTEM_PROMPT_PR_WALKTHROUGH_ARTIFACT_COMMAND_VAR_0
  - SYSTEM_PROMPT_PR_WALKTHROUGH_ARTIFACT_COMMAND_VAR_1
  - SYSTEM_PROMPT_PR_WALKTHROUGH_ARTIFACT_COMMAND_VAR_2
  - SYSTEM_PROMPT_PR_WALKTHROUGH_ARTIFACT_COMMAND_VAR_3
  - SYSTEM_PROMPT_PR_WALKTHROUGH_ARTIFACT_COMMAND_VAR_4
  - SYSTEM_PROMPT_PR_WALKTHROUGH_ARTIFACT_COMMAND_VAR_5
  - SYSTEM_PROMPT_PR_WALKTHROUGH_ARTIFACT_COMMAND_VAR_6
  - SYSTEM_PROMPT_PR_WALKTHROUGH_ARTIFACT_COMMAND_2_VAR_7
-->
${SYSTEM_PROMPT_PR_WALKTHROUGH_ARTIFACT_COMMAND_VAR_0===""?SYSTEM_PROMPT_PR_WALKTHROUGH_ARTIFACT_COMMAND_VAR_1:SYSTEM_PROMPT_PR_WALKTHROUGH_ARTIFACT_COMMAND_VAR_2(SYSTEM_PROMPT_PR_WALKTHROUGH_ARTIFACT_COMMAND_VAR_0)}
${SYSTEM_PROMPT_PR_WALKTHROUGH_ARTIFACT_COMMAND_VAR_3?`
Additional guidance from the user: ${SYSTEM_PROMPT_PR_WALKTHROUGH_ARTIFACT_COMMAND_VAR_3}
`:""}
## Goal

Produce a **shareable PR walkthrough artifact** — a self-contained HTML page a
reviewer can read before opening the diff to understand what this change does,
why it's being made, and where to focus attention. Pitch the writing at a
reviewer seeing this PR for the first time.

${SYSTEM_PROMPT_PR_WALKTHROUGH_ARTIFACT_COMMAND_VAR_4}

## Build it from the explainer template

Load the \`artifact-explainer\` skill and build the page from its template,
publishing with the ${SYSTEM_PROMPT_PR_WALKTHROUGH_ARTIFACT_COMMAND_VAR_5} tool as that skill directs. Use the
template's **sections flavor** — keep the sections structure, delete the
numbered steps. Fill the slots as follows:

- **Lede** — what this PR changes and why it's needed, in two or three
  sentences. If the PR body already says this well, reuse it.
- **Sections** — open with a before/after section showing the user-observable
  change (behavior, API shape, or output); skip it if the change has no
  observable surface. Group the diff into sections cut at its joints — related
  changes together, not one section per file. Each section is usually a
  trimmed snippet, a plain-language explanation, and anything a reviewer
  should look closely at. PR walkthroughs are mostly symbolic content, so
  default to code — add a diagram only where structure or flow genuinely needs
  one, not the skill's diagram-first opener. End with a section for what's
  *not* obvious from the diff: why this approach over an alternative, what was
  tried and rejected, follow-ups intentionally left out.
- **Recap** — restate the takeaways as where a reviewer should focus
  attention.

End the page body with this line verbatim:

> ${SYSTEM_PROMPT_PR_WALKTHROUGH_ARTIFACT_COMMAND_VAR_6}

${SYSTEM_PROMPT_PR_WALKTHROUGH_ARTIFACT_COMMAND_2_VAR_7}
