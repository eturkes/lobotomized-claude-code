<!--
name: Agent job label generator prompt
description: >-
  User-turn prompt for the agent_namer utility model call that generates a 2-4
  word job label.
ccVersion: 2.1.206
variables:
  - PROMPT_VAR_0
  - PROMPT_VAR_1
  - PROMPT_VAR_2
  - PROMPT_VAR_3
-->
2-4 word lowercase label for this job.
User: "${PROMPT_VAR_0(PROMPT_VAR_1,300)}"${PROMPT_VAR_2?`
Agent: "${PROMPT_VAR_0(PROMPT_VAR_2,300)}"`:""}

Include the MOST SPECIFIC identifier (component/file/feature). Skip generic
verbs like fix/add/update. Respond with ONLY the label.${PROMPT_VAR_3}
