<!--
name: 'Skill: Code Review (--fix applying fixes)'
description: >-
  Appended to the code-review prompt when --fix is passed; instructs applying
  each finding to the working tree, skipping behavior-changing or out-of-scope
  fixes
ccVersion: 2.1.204
variables:
  - SKILL_CODE_REVIEW_APPLYING_FIXES_VAR_0
  - SKILL_CODE_REVIEW_APPLYING_FIXES_VAR_1
-->


## Applying fixes (--fix)

The \`--fix\` flag was passed. After producing the findings list, apply the
findings to the working tree instead of stopping at the report: fix each one
directly — correctness bugs and reuse/simplification/efficiency cleanups alike.
Skip any finding whose fix would change intended behavior, require changes well
outside the reviewed diff, or that you judge to be a false positive — note the
skip rather than arguing with it. ${SKILL_CODE_REVIEW_APPLYING_FIXES_VAR_0?`Then call ${SKILL_CODE_REVIEW_APPLYING_FIXES_VAR_1} again with the same findings, each
carrying an \`outcome\`: \`fixed\`, \`no_change_needed\` (the finding was wrong or
already handled), or \`skipped\` (real but not applied). Do not repeat the
findings as text; after the call, give one line per skipped finding saying why.`:`Finish with a brief summary of what was fixed
and what was skipped.`}
