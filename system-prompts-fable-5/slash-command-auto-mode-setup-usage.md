<!--
name: /auto-mode-setup usage text
description: >-
  Usage string returned as JSON reason by the non-interactive /auto-mode-setup
  local command; surfaced to the model via local-command-stdout.
ccVersion: 2.1.210
-->
Usage:
  /auto-mode-setup --wizard posture=<personal|open-source|enterprise|mixed> scope=<all|project> depth=<both|shell|repos|here> --propose
  /auto-mode-setup --apply-file <absolute-path>   (reads a proposal JSON from a file under the system temp dir or the Claude config dir — the caller must have shown it to the user first)
