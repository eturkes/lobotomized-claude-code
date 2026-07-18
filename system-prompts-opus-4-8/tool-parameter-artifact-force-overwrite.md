<!--
name: 'Tool Parameter: Artifact Force Overwrite'
description: >-
  artifact tool force param: overwrite without conflict check; use only after a
  409 once reconciled, else omit so concurrent writes 409.
ccVersion: 2.1.214
-->
Overwrite without a conflict check. Use only after a 409 once you have reconciled with the other session's version and intend to replace it. baseVersion is always sent; with force:true the server treats it as informational and overwrites. Omit (or false) so a concurrent write 409s instead of being clobbered.
