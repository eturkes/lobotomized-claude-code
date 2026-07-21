<!--
name: 'Tool Parameter: Artifact supporting files'
description: >-
  Top-level `files` param of the artifact publish tool: map or list of
  supporting files published alongside the page.
ccVersion: null
-->
Supporting files to publish alongside the page. Map form {"published/path": "source/path" | {from, contentType}} publishes each source at the key (what the HTML references); list form publishes each file at its own spelling. Sources must lie under the working directory.
