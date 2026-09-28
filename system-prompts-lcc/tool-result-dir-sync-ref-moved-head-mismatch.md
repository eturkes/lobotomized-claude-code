<!--
name: 'Dir-sync: ref moved right after update, index left as-is'
description: >-
  Reason detail for a git ref-move check failing because the branch did not name
  the session's HEAD right after the update was reported, so the index was left
  unchanged.
ccVersion: 2.1.284
-->
the branch did not name the session's HEAD right after git reported the update (moved again at once, or the write did not land where it was read): the index was left as it was
