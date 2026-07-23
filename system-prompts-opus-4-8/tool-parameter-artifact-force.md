<!--
name: 'Tool Parameter: Artifact force'
description: >-
  Description of the Artifact tool's `force` boolean input parameter, delivered
  to the model as part of the tool's input_schema.
ccVersion: 2.1.218
-->
Last-resort overwrite that DISCARDS another session's published version. On a 409 the normal fix is to re-read the artifact, merge your edits onto the newer content, and publish again — not force. Use force:true only when the user explicitly wants to replace the other session's version. baseVersion is still sent; with force:true the server treats it as informational and overwrites. Omit (or false) so a concurrent write 409s instead of being clobbered.
