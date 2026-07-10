<!--
name: Config key-value situation
description: >-
  The situation string of the "config-key-value" usage-nudge object, injected
  into model context as part of the usage-nudge catalog.
ccVersion: 2.1.206
-->
User opens the /config panel (or asks how to change a setting) for a panel setting — model, theme, verbose, thinking, output style, editor, or similar — and navigates the menu to flip one toggle. They are using the interactive panel for something the inline syntax does in one line. IMPORTANT: Do NOT match edits to hooks, permissions, env, statusLine, or other structured settings.json keys — those are not /config key=value keys.
