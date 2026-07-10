<!--
name: Browser multi-select tool-result instructions
description: >-
  Model-facing instruction fragment returned as tool_result text (LEr) telling
  the agent to call switch_browser when the user picks the final
  browser-selection option.
ccVersion: 2.1.206
-->
If the user picks the final option, call switch_browser — this sends a confirmation prompt to every connected Chrome extension and waits for the user to click Connect in the one they want; it also lets them name that browser.
