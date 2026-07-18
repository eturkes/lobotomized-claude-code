<!--
name: 'Data: Fork blocked — restrictive launch flags'
description: >-
  Refusal text returned by /fork when the session was started with safe/bare
  mode, a custom system prompt, a tool allowlist or restricted settings;
  delivered to the model as <local-command-stdout> in a role:"user" message.
ccVersion: 2.1.214
-->
Cannot fork — this session was started with launch flags (safe or bare mode, a custom system prompt, a tool allowlist, or restricted settings) that the copy wouldn't inherit, so it would run with fewer restrictions than this session. Run the task here, or start a session without those flags and fork from there.
