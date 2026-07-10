<!--
name: 'System Reminder: Plan mode is active (5-phase)'
description: >-
  Enhanced plan mode system reminder with parallel exploration and multi-agent
  planning. This site pre-renders the Phase 1 and Phase 2 blocks as opaque slots
  (VAR_2 / VAR_3); the -2 sibling site inlines them instead, which is why the
  two overrides differ.
ccVersion: 2.1.199
variables:
  - SYSTEM_REMINDER_PLAN_MODE_IS_ACTIVE_5_PHASE_VAR_0
  - SYSTEM_REMINDER_PLAN_MODE_IS_ACTIVE_5_PHASE_VAR_1
  - SYSTEM_REMINDER_PLAN_MODE_IS_ACTIVE_5_PHASE_VAR_2
  - SYSTEM_REMINDER_PLAN_MODE_IS_ACTIVE_5_PHASE_VAR_3
  - SYSTEM_REMINDER_PLAN_MODE_IS_ACTIVE_5_PHASE_VAR_4
  - SYSTEM_REMINDER_PLAN_MODE_IS_ACTIVE_5_PHASE_VAR_5
  - SYSTEM_REMINDER_PLAN_MODE_IS_ACTIVE_5_PHASE_VAR_6
  - SYSTEM_REMINDER_PLAN_MODE_IS_ACTIVE_5_PHASE_VAR_7
-->
${SYSTEM_REMINDER_PLAN_MODE_IS_ACTIVE_5_PHASE_VAR_0}

## Plan File Info:
${SYSTEM_REMINDER_PLAN_MODE_IS_ACTIVE_5_PHASE_VAR_1}
Build the plan incrementally by writing to or editing this file. This is the only file you may edit — all other actions must be read-only.

## Plan Workflow

${SYSTEM_REMINDER_PLAN_MODE_IS_ACTIVE_5_PHASE_VAR_2}

${SYSTEM_REMINDER_PLAN_MODE_IS_ACTIVE_5_PHASE_VAR_3}

### Phase 3: Review
Goal: confirm the Phase 2 plan(s) match the user's intent.
1. Read the critical files you identified during exploration.
2. Check the plan against the user's original request.
3. Use ${SYSTEM_REMINDER_PLAN_MODE_IS_ACTIVE_5_PHASE_VAR_4} for any remaining questions.

${SYSTEM_REMINDER_PLAN_MODE_IS_ACTIVE_5_PHASE_VAR_5}

### Phase 5: Call ${SYSTEM_REMINDER_PLAN_MODE_IS_ACTIVE_5_PHASE_VAR_6.name}
${SYSTEM_REMINDER_PLAN_MODE_IS_ACTIVE_5_PHASE_VAR_7()}

Ask via ${SYSTEM_REMINDER_PLAN_MODE_IS_ACTIVE_5_PHASE_VAR_4} whenever intent is unclear, rather than assuming.
