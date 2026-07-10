<!--
name: /loop usage text
description: >-
  Usage/help text for /loop returned via getPromptForCommand as {type:text} when
  invoked without a valid prompt, sent to the model.
ccVersion: 2.1.206
variables:
  - SLASH_COMMAND_LOOP_USAGE_2_VAR_0
-->
Usage: /loop [interval] <prompt>

Run a prompt or slash command on a recurring interval.

Intervals: Ns, Nm, Nh, Nd (e.g. 5m, 30m, 2h, 1d). Minimum granularity is 1 minute.
If no interval is specified, defaults to ${SLASH_COMMAND_LOOP_USAGE_2_VAR_0}.

Examples:
  /loop 5m /babysit-prs
  /loop 30m check the deploy
  /loop 1h /standup 1
  /loop check the deploy          (defaults to ${SLASH_COMMAND_LOOP_USAGE_2_VAR_0})
  /loop check the deploy every 20m
