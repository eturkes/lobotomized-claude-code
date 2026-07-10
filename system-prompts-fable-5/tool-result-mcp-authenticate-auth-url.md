<!--
name: 'MCP authenticate: authorization URL'
description: >-
  Tool-result message from MCP authenticate asking the user to open the
  authorization URL.
ccVersion: 2.1.206
variables:
  - TOOL_RESULT_MCP_AUTHENTICATE_AUTH_URL_VAR_0
  - TOOL_RESULT_MCP_AUTHENTICATE_AUTH_URL_VAR_1
  - TOOL_RESULT_MCP_AUTHENTICATE_AUTH_URL_VAR_2
-->
Ask the user to open this URL in their browser to authorize the ${TOOL_RESULT_MCP_AUTHENTICATE_AUTH_URL_VAR_0} MCP server:

${TOOL_RESULT_MCP_AUTHENTICATE_AUTH_URL_VAR_1}

Once they complete the flow, the server's tools will become available automatically.${TOOL_RESULT_MCP_AUTHENTICATE_AUTH_URL_VAR_2}
