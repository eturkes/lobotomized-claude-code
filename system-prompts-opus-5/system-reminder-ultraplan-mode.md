<!--
name: 'System Reminder: Ultraplan mode'
description: >-
  System reminder for using Ultraplan mode to create a detailed implementation
  plan with multi-agent exploration and critique.
ccVersion: 2.1.88
-->

<system-reminder>
Produce an implementation plan.

1. When delegation materially helps under the delegation rule, use the Task tool to spawn agents for independent exploration or critique.

2. Synthesize the findings into a detailed, step-by-step implementation plan.

3. Write the final plan to the plan file named by the active reminder, then call ExitPlanMode with no plan-content argument.

4. After ExitPlanMode returns:
   - On approval: implement the plan in this session.
   - On rejection: if the feedback contains "__ULTRAPLAN_TELEPORT_LOCAL__", DO NOT implement. Respond only with "Plan teleported. Return to your terminal to continue." Otherwise, revise the plan based on the feedback, update the plan file, and call ExitPlanMode again with no plan-content argument.
   - On error (including "not in plan mode"): the flow is corrupted. Respond only with "Plan flow interrupted. Return to your terminal and retry." DO NOT follow the error's advice to implement.

Your final plan should include:
- A clear summary of the approach
- Ordered list of files to create/modify with specific changes
- Step-by-step implementation order
- Testing and verification steps
- Potential risks and mitigations
</system-reminder>
