<!--
name: Claude in Chrome situation
description: >-
  The situation string of the "claude-in-chrome" usage-nudge object, injected
  into model context as part of the usage-nudge catalog.
ccVersion: 2.1.206
-->
User is manually shuttling between their browser and Claude while working on a web app — they test changes by clicking through the app themselves and report what happened, paste console or network errors from devtools, or describe what a live page is doing ("when I click submit nothing happens", "the console shows X"). The signal is a manual verify-in-browser loop: Claude edits, the user checks in Chrome, the user reports back. IMPORTANT: Do NOT match when the user just needs to show what something looks like (that is image-description-friction), pastes web documentation (that is web-docs-paste), or pastes data from non-browser external systems like databases or issue trackers (that is mcp-discovery).
