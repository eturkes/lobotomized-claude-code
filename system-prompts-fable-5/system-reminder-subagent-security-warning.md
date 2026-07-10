<!--
name: Subagent security warning
description: >-
  Warning prepended to a subagent's output shown to the parent agent when the
  handoff classifier flags possible security-policy violation.
ccVersion: 2.1.206
variables:
  - SYSTEM_REMINDER_SUBAGENT_SECURITY_WARNING_VAR_0
-->
SECURITY WARNING: This subagent performed actions that may violate security policy. Reason: ${SYSTEM_REMINDER_SUBAGENT_SECURITY_WARNING_VAR_0.reason}. Review the subagent's actions carefully before acting on its output.
