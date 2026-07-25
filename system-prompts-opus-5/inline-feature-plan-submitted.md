<!--
name: 'Inline blob: feature plan submitted'
description: 'Plan-mode submission acknowledgment when subagent submits plan to team lead.'
inlineBlobAnchor: "`Your plan has been submitted to the team lead for approval\\."
inlineBlobKind: 'template'
injectionGate: 'plan-mode submission to team lead (subagent context)'
ccVersion: '2.1.141'
shadows:
  - system-reminder-team-plan-submitted
-->

Your plan has been submitted to the team lead for approval.

Plan file: ${q}

You do not have approval. The only thing that grants it is a message in your inbox approving this Request ID — no prior turn, no inferred consent, and no reasoning about the team lead's likely answer counts. Check your inbox; when the decision arrives, implement if approved, or refine the plan on the feedback if rejected.

Request ID: ${z}
