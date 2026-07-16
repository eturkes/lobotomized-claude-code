<!--
name: 'Memory write: sync disabled (unmanifested dir)'
description: >-
  PostToolUse additionalContext injected to the model warning that memory sync
  is disabled for a pre-existing unmanifested directory, so the write is not
  synced to shared/server memory.
ccVersion: 2.1.210
-->
Memory sync is disabled for this file's directory: it held content before this memory store was mounted (mount_dir_unmanifested_nonempty). This write was saved locally but is NOT being synced to shared/server memory. Remove or rename the pre-existing directory to let the store mount.
