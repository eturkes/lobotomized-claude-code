<!--
name: Subagent security-policy violation warning
description: >-
  Security warning prepended to sub-agent output when the handoff classifier
  flags a possible policy violation, shown to the parent model.
ccVersion: 2.1.210
variables:
  - TOOL_RESULT_SUBAGENT_SECURITY_POLICY_WARNING_VAR_0
  - TOOL_RESULT_SUBAGENT_SECURITY_POLICY_WARNING_VAR_1
-->
SECURITY WARNING: This subagent performed actions that may violate security policy. Reason: ${TOOL_RESULT_SUBAGENT_SECURITY_POLICY_WARNING_VAR_0(TOOL_RESULT_SUBAGENT_SECURITY_POLICY_WARNING_VAR_1.reason,{prependMarker:!1}).sanitized}. Review the subagent's actions carefully before acting on its output.
