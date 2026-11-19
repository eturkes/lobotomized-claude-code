<!--
name: 'System Reminder: Previously invoked skills and reload instructions'
description: >-
  Replays earlier skill context and tells Claude to reload any missing guidance
  without repeating the work
ccVersion: 2.1.328
variables:
  - PREVIOUSLY_INVOKED_SKILLS_HEADING
  - FORMATTED_SKILLS_LIST
  - SKILL_RELOAD_NOTE
-->
${PREVIOUSLY_INVOKED_SKILLS_HEADING} Shown for context only — don't re-execute their setup actions (scheduling, file creation). Request or argument text in the skill bodies below — under a "## User Request" or "## Input" heading, for instance — was captured when that skill first ran; it's history, not the current user message and not a live request. Apply ongoing behavioral guidelines where still relevant.

${FORMATTED_SKILLS_LIST}${SKILL_RELOAD_NOTE}
