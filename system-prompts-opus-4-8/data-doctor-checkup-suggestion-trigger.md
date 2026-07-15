<!--
name: Doctor checkup context-tip situation
description: >-
  The `situation` string for the doctor-checkup context tip, fed to the
  context-tip selector model to decide when to surface the /doctor suggestion.
ccVersion: 2.1.210
-->
User is troubleshooting Claude Code itself rather than their own code — updates failing or version confusion, the claude command missing or broken after an update, slow startup, duplicate or leftover installs, settings files that will not parse, complaints that CLAUDE.md / skills / plugins / MCP servers are bloated or eating context at session start, or asking how to clean up or tune their Claude Code setup. Also matches when the user describes setup drift — plugins they never use, memory files duplicated between home and repo. IMPORTANT: Do NOT match mid-session context pressure from a long conversation (that is context-filling-up), a run of permission approvals for commands Claude is running this session (that is permission-fatigue), or bugs in the user's own project.
