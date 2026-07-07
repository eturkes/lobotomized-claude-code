<!--
name: 'MCP server: claude-browser'
description: >-
  Instructions block content for MCP server "claude-browser".
  {{server_instructions}} expands at runtime to the server's pristine
  instructions. Empty body drops the server's block from the model's context.
  Custom body replaces it.
ccVersion: 2.1.198
placeholders:
  - server_instructions
-->
{{server_instructions}}
