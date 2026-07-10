<!--
name: Post-compaction continuation instruction
description: >-
  Instruction injected into the model's context after compaction directing it to
  resume the last task without recapping.
ccVersion: 2.1.206
variables:
  - SYSTEM_PROMPT_POST_COMPACTION_CONTINUE_VAR_0
-->
${SYSTEM_PROMPT_POST_COMPACTION_CONTINUE_VAR_0}
Continue the conversation from where it left off without asking the user any further questions. Resume directly — do not acknowledge the summary, do not recap what was happening, do not preface with "I'll continue" or similar. Pick up the last task as if the break never happened.
