<!--
name: 'Tool Parameter: Artifact multi-file root base directory'
description: >-
  The Artifact publishing tool's `root` parameter — base dir that relative
  SOURCE paths resolve against.
ccVersion: null
-->
Base directory that relative SOURCE paths resolve against (like a bundler root) — saves retyping a long build prefix. Never changes published paths. Absolute, or relative to the working directory; must lie within it. Requires `files`.
