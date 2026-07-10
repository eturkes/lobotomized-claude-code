<!--
name: Permission param match situation
description: >-
  The situation string of the "permission-param-match" usage-nudge object,
  injected into model context as part of the usage-nudge catalog.
ccVersion: 2.1.206
-->
User has denied (or chosen "ask every time" for) the same tool-call pattern more than once while approving other calls of the same tool — e.g., rejecting Agent whenever it requests a specific model, or Bash whenever it wants to run in the background. They are manually filtering on a parameter value each time the prompt appears. IMPORTANT: Do NOT match a single one-off denial, or blanket denial of a tool regardless of parameters.
