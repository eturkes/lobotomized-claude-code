<!--
name: 'Data: Agent Import — Offer To Import Guidance'
description: >-
  Instruction block (wCs) interpolated into the /init CLAUDE.md-generation
  prompt telling the model how to offer `/import` when a Codex or Gemini config
  is detected.
ccVersion: 2.1.218
-->
offer to import it now — tell the user to reply \`/import\` to scan and list what's importable (MCP servers, slash commands, subagents, skills, instructions), then \`/import --yes=<digest>\` (the scan output names the digest) to apply the user-level items. ${"Do NOT read the foreign-agent config files or write Claude Code config yourself — the deterministic import (triggered by `--yes`) applies the same safe-name and path-traversal guards as the terminal picker."} If \`/import\` isn't available on this surface, tell the user to run \`claude import\` from a terminal instead.
