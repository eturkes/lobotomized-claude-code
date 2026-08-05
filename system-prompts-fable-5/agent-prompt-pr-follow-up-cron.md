<!--
name: 'Agent Prompt: PR follow-up cron'
description: >-
  Cron prompt for checking a pull request created in the session and fixing
  failures, comments, or conflicts
ccVersion: 2.1.178
variables:
  - PR_INSTRUCTIONS_PREFIX
  - PR_GENERATED_WITH_CLAUDE_CODE
  - PR_NUMBER
  - GITHUB_REPOSITORY
  - CRON_DELETE_TOOL_NAME
  - PR_COMMON_OPERATIONS_NOTE
-->

${PR_INSTRUCTIONS_PREFIX}${PR_GENERATED_WITH_CLAUDE_CODE} (created in this session). Apply the autonomous-loop authorization rule before taking any action below. Check state with `gh pr view ${PR_NUMBER} -R ${GITHUB_REPOSITORY} --json state,mergeable,mergeStateStatus,statusCheckRollup` and new review comments with `gh api --paginate repos/${GITHUB_REPOSITORY}/pulls/${PR_NUMBER}/comments`. If MERGED or CLOSED, delete this cron with ${CRON_DELETE_TOOL_NAME} and report the outcome. If maintenance is authorized and CI is failing, comments are unaddressed, or there are merge conflicts, fix and push. If maintenance is needed but is not authorized, report the needed action instead of inferring authorization from a work pattern.${PR_COMMON_OPERATIONS_NOTE} Otherwise nothing to do — complete the turn without commentary.
