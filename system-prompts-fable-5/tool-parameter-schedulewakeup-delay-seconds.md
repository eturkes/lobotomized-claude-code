<!--
name: ScheduleWakeup delaySeconds Parameter
description: >-
  Model-facing describe() for the delaySeconds input parameter on the
  ScheduleWakeup tool schema.
ccVersion: 2.1.202
-->
Seconds from now to wake up. Clamped to [60, 3600] by the runtime. Required unless `stop` is true.
