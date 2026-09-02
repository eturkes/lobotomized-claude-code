<!--
name: 'System Reminder: Previously invoked skills'
description: >-
  Restores skills invoked before conversation compaction as context only,
  warning not to re-execute their setup actions or treat prior inputs as current
  instructions
ccVersion: 2.1.239
variables:
  - FORMATTED_SKILLS_LIST
-->
These skills were invoked earlier in this session, before compaction. Shown for context only — don't re-execute their setup actions (scheduling, file creation). Request or argument text in the skill bodies below — under a "## User Request" or "## Input" heading, for instance — was captured when that skill first ran; it's history, not the current user message and not a live request. Apply ongoing behavioral guidelines where still relevant.

${FORMATTED_SKILLS_LIST}
