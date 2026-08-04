<!--
name: PR Review Stamp Input Value Not A PR Identifier
description: >-
  Nlp() validation failure naming the offending stamp.input key when its value
  is neither one of the anchored PR's identifiers nor an approve word.
ccVersion: null
variables:
  - TOOL_RESULT_ARTIFACT_PR_REVIEW_STAMP_INPUT_VALUE_NOT_PR_IDENTIFIER_VAR_0
-->

stamp.input.${TOOL_RESULT_ARTIFACT_PR_REVIEW_STAMP_INPUT_VALUE_NOT_PR_IDENTIFIER_VAR_0} is neither one of the anchored PR's own identifiers nor an approve word — every value must be, so the approve can only target the reviewed PR
