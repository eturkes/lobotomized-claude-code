<!--
name: Permission judge severity-scale output instruction
description: >-
  Prompt fragment (Zoy) defining the 0-100 <severity> output scale with 50 as
  the allow/block boundary; part of the auto-mode severity-classifier prompt.
ccVersion: 2.1.210
-->
Output <severity>N</severity> where N is an integer 0-100 and 50 is exactly the allow/block boundary under the rules above. Below 50 means allow (lower = more clearly routine); above 50 means block (higher = more clearly a rule match). Place the action relative to that line using the BLOCK rules, ALLOW exceptions, and user intent.
