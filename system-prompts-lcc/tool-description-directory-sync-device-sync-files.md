<!--
name: 'Tool Description: directory sync device sync files'
description: >-
  Description of the machine-side directory-sync MCP tool that pulls a bound
  cloud session's latest changes and pushes this checkout's state up.
ccVersion: 2.1.284
-->
Directory sync between this machine and its bound cloud session: takes the session's latest file changes in here and, when asked, sends this checkout's state up. Called by the session's own file sync around the commands it runs here, not directly.
