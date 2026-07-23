<!--
name: 'Tool Result: Forked-Skill Spawn Limit Past Depth Cap'
description: >-
  TelemetrySafeError thrown by the forked-skill spawn path when the session
  spawn cap is hit past the nesting depth cap, telling the model to do the
  skill's work inline; surfaced to the model as the Skill tool's
  <tool_use_error> or as <local-command-stderr> message content.
ccVersion: 2.1.218
variables:
  - TOOL_RESULT_FORKED_SKILL_SPAWN_LIMIT_DEPTH_CAP_VAR_0
  - TOOL_RESULT_FORKED_SKILL_SPAWN_LIMIT_DEPTH_CAP_VAR_1
-->
Subagent spawn limit reached (${TOOL_RESULT_FORKED_SKILL_SPAWN_LIMIT_DEPTH_CAP_VAR_0} of ${TOOL_RESULT_FORKED_SKILL_SPAWN_LIMIT_DEPTH_CAP_VAR_1}) past the nesting depth cap. Do the skill's work directly in this context instead of invoking further skills.
