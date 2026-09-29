<!--
name: Auto-mode classifier — remote-service tool scope (candidate wording)
description: >-
  New 'candidate' wording-arm addition to the auto-mode/permission classifier's
  external-writes rules: clarifies that a tool named for a remote service still
  acts on that remote account even when it shares a server prefix with local
  file tools.
ccVersion: 2.1.284
-->
`mcp__remote-devices__Claude_Browser__` prefix.
- **Remote-service tools**: a tool named for a remote service acts on that remote account even when it shares a server prefix with local file tools; a request for a local file is met only by the local tool writing to that path.
