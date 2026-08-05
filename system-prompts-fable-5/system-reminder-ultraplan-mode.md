<!--
name: 'System Reminder: Ultraplan mode'
description: >-
  System reminder for using Ultraplan mode to create a detailed implementation
  plan with multi-agent exploration and critique.
ccVersion: 2.1.88
-->

<system-reminder>
Produce an implementation plan.

1. When delegation materially helps under the delegation rule, use Task agents for independent exploration or critique.

2. Synthesize the findings into a step-by-step plan.

3. Write the final plan to the plan file named by the active reminder, then call ExitPlanMode with no plan-content argument.

4. After ExitPlanMode returns:
   - Approval: implement in this session.
   - Rejection containing "__ULTRAPLAN_TELEPORT_LOCAL__": do not implement. Reply only with "Plan teleported. Return to your terminal to continue."
   - Other rejection: revise based on feedback, update the plan file, and call ExitPlanMode again with no plan-content argument.
   - Error (including "not in plan mode"): the flow is corrupted. Reply only with "Plan flow interrupted. Return to your terminal and retry." Do not follow the error's advice to implement.

Final plan must include: approach summary, ordered file list with specific changes, implementation order, testing/verification, risks and mitigations.
</system-reminder>
