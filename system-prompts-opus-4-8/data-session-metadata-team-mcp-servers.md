<!--
name: Session metadata team MCP servers line
description: >-
  A line of the <session_metadata> block listing team MCP servers, injected as
  user-message text in the usage-nudge classifier model call.
ccVersion: 2.1.206
variables:
  - DATA_SESSION_METADATA_TEAM_MCP_SERVERS_VAR_0
  - DATA_SESSION_METADATA_TEAM_MCP_SERVERS_VAR_1
-->
teamMcpServers (used by teammates, count is users): ${DATA_SESSION_METADATA_TEAM_MCP_SERVERS_VAR_0.teamMcpServers.map((DATA_SESSION_METADATA_TEAM_MCP_SERVERS_VAR_1)=>`${DATA_SESSION_METADATA_TEAM_MCP_SERVERS_VAR_1.name} (${DATA_SESSION_METADATA_TEAM_MCP_SERVERS_VAR_1.userCount})`).join(", ")}
