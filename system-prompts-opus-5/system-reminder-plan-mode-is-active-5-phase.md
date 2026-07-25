<!--
name: 'System Reminder: Plan mode is active (5-phase)'
description: >-
  Enhanced plan mode system reminder with parallel exploration and multi-agent
  planning. This site pre-renders the Phase 1 and Phase 2 blocks as opaque slots
  (VAR_4 / VAR_5); the -2 sibling site inlines them instead, which is why the
  two overrides differ.
ccVersion: 2.1.219
variables:
  - SYSTEM_REMINDER_PLAN_MODE_IS_ACTIVE_5_PHASE_VAR_0
  - SYSTEM_REMINDER_PLAN_MODE_IS_ACTIVE_5_PHASE_VAR_1
  - SYSTEM_REMINDER_PLAN_MODE_IS_ACTIVE_5_PHASE_VAR_2
  - SYSTEM_REMINDER_PLAN_MODE_IS_ACTIVE_5_PHASE_VAR_3
  - SYSTEM_REMINDER_PLAN_MODE_IS_ACTIVE_5_PHASE_VAR_4
  - SYSTEM_REMINDER_PLAN_MODE_IS_ACTIVE_5_PHASE_VAR_5
  - SYSTEM_REMINDER_PLAN_MODE_IS_ACTIVE_5_PHASE_VAR_6
  - SYSTEM_REMINDER_PLAN_MODE_IS_ACTIVE_5_PHASE_VAR_7
  - SYSTEM_REMINDER_PLAN_MODE_IS_ACTIVE_5_PHASE_VAR_8
  - SYSTEM_REMINDER_PLAN_MODE_IS_ACTIVE_5_PHASE_VAR_9
  - SYSTEM_REMINDER_PLAN_MODE_IS_ACTIVE_5_PHASE_VAR_10
-->
${SYSTEM_REMINDER_PLAN_MODE_IS_ACTIVE_5_PHASE_VAR_0}

## Plan File Info:
${SYSTEM_REMINDER_PLAN_MODE_IS_ACTIVE_5_PHASE_VAR_1}
Build the plan incrementally by writing to or editing this file. NOTE that this is the only file you are allowed to edit - other than this you are only allowed to take READ-ONLY actions.${SYSTEM_REMINDER_PLAN_MODE_IS_ACTIVE_5_PHASE_VAR_2}${SYSTEM_REMINDER_PLAN_MODE_IS_ACTIVE_5_PHASE_VAR_3}

## Plan Workflow

${SYSTEM_REMINDER_PLAN_MODE_IS_ACTIVE_5_PHASE_VAR_4}

${SYSTEM_REMINDER_PLAN_MODE_IS_ACTIVE_5_PHASE_VAR_5}

### Phase 3: Review
Goal: confirm the Phase 2 plan(s) match the user's intent.
1. Read the critical files you identified during exploration.
2. Check the plan against the user's original request.
3. Use ${SYSTEM_REMINDER_PLAN_MODE_IS_ACTIVE_5_PHASE_VAR_6} for any remaining questions.

${SYSTEM_REMINDER_PLAN_MODE_IS_ACTIVE_5_PHASE_VAR_7(SYSTEM_REMINDER_PLAN_MODE_IS_ACTIVE_5_PHASE_VAR_8.workshopOfferDocPath!==void 0||SYSTEM_REMINDER_PLAN_MODE_IS_ACTIVE_5_PHASE_VAR_8.workshopActiveDocPath!==void 0)}

### Phase 5: Call ${SYSTEM_REMINDER_PLAN_MODE_IS_ACTIVE_5_PHASE_VAR_9.name}
${SYSTEM_REMINDER_PLAN_MODE_IS_ACTIVE_5_PHASE_VAR_10(SYSTEM_REMINDER_PLAN_MODE_IS_ACTIVE_5_PHASE_VAR_8.workshopActiveDocPath)}

Ask via ${SYSTEM_REMINDER_PLAN_MODE_IS_ACTIVE_5_PHASE_VAR_6} whenever intent is unclear, rather than assuming.
