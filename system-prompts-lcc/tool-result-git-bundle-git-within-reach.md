<!--
name: 'Tool Result: git bundle git within reach'
description: >-
  Cloud-session creation failure telling the model git was found only in
  directories cloud sessions on this machine can write to, so it was not run,
  and how to relocate git so first-upload preparation can proceed.
ccVersion: 2.1.284
variables:
  - TOOL_RESULT_GIT_BUNDLE_GIT_WITHIN_REACH_VAR_0
-->
git was found only in directories that cloud sessions on this machine can write to, so it was not run. Install git somewhere they cannot write to — outside this project directory, outside their temporary directories, and outside your home directory when git tracks your home or a folder above it — make sure that directory is on PATH as an absolute path, and restart Claude Code.${TOOL_RESULT_GIT_BUNDLE_GIT_WITHIN_REACH_VAR_0()}
