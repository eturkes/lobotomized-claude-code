<!--
name: 'Tool Result: Artifact Stale-Version Guard Workshop Read Instruction'
description: >-
  Branch of the artifact stale-version guard error telling the model to re-read
  a workshop page via read_page_data with the workshop-decisions schema instead
  of WebFetch/force.
ccVersion: 2.1.218
-->
for a workshop page use the read_page_data action with schema "workshop-decisions" — the workshop skill forbids WebFetch and force there; otherwise WebFetch the URL
