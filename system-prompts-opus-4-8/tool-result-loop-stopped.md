<!--
name: Loop Stopped — No Further Wakeups
description: >-
  Model-facing tool_result telling the model the dynamic loop has stopped with
  no further wakeups scheduled, and to trigger any armed wakeup/timer it set.
ccVersion: 2.1.202
variables:
  - TOOL_RESULT_LOOP_STOPPED_VAR_0
  - TOOL_RESULT_LOOP_STOPPED_VAR_1
-->
Loop stopped — no further wakeups scheduled. If you armed a ${TOOL_RESULT_LOOP_STOPPED_VAR_0} for this loop, ${TOOL_RESULT_LOOP_STOPPED_VAR_1} it now; otherwise nothing more to do this turn.
