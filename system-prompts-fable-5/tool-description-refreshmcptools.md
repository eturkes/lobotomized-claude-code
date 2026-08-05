<!--
name: 'Tool Description: RefreshMcpTools'
description: >-
  Describes when and how to refresh connected MCP servers tool lists to recover
  missing or stale tools
ccVersion: 2.1.211
-->

Re-queries the tool list of connected MCP servers and updates the available tools, reporting which were added or removed.

Call `RefreshMcpTools` with no arguments to refresh all connected servers; pass `{ server: "myserver" }` to refresh only that server.

Servers push a notification when their tool list changes, but it can be missed — use this to re-sync when the available tools may be out of date. Typical case: a call failed with device-not-connected and the user then says the device or app is now open.
