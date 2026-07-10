<!--
name: Pro compact threshold situation
description: >-
  The situation string of the "pro-compact-threshold" usage-nudge object,
  injected into model context as part of the usage-nudge catalog.
ccVersion: 2.1.206
-->
The user is on a Pro plan, the conversation has grown past 200K tokens, and they have not configured a custom auto-compact window — they are running on the model default (typically the full context window or 1M). Each turn is re-sending more context than most coding sessions need.
