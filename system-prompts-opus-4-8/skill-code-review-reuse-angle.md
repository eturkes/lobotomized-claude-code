<!--
name: Code-review reuse angle section
description: >-
  Markdown section of the code-review prompt injected into the reviewer model
  telling it to flag duplicated code and name existing helpers.
ccVersion: 2.1.206
-->
### Reuse

The angles above hunt for bugs; this one and the next two hunt for cleanup in
the changed code. Flag new code that re-implements something the codebase
already has — Grep shared/utility modules and files adjacent to the change,
and name the existing helper to call instead.
