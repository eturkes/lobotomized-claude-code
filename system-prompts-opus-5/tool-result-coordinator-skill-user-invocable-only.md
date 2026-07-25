<!--
name: Coordinator skill user-invocable-only block
description: >-
  Meta message returned when a coordinator tries to run a
  disable-model-invocation skill that only the user may invoke.
ccVersion: 2.1.210
variables:
  - TOOL_RESULT_COORDINATOR_SKILL_USER_INVOCABLE_ONLY_VAR_0
  - TOOL_RESULT_COORDINATOR_SKILL_USER_INVOCABLE_ONLY_VAR_1
-->
Skill "/${TOOL_RESULT_COORDINATOR_SKILL_USER_INVOCABLE_ONLY_VAR_0.name}" is user-invocable only (disable-model-invocation) and cannot run in coordinator mode: the coordinator does not load skill content, and workers cannot invoke it via the ${TOOL_RESULT_COORDINATOR_SKILL_USER_INVOCABLE_ONLY_VAR_1} tool.
