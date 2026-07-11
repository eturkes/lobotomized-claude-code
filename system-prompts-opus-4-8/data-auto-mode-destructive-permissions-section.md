<!--
name: 'Data: Auto-mode destructive permissions.allow section'
description: >-
  Runtime-built markdown section listing destructive permissions.allow entries,
  assembled by noe()/vyb() into the auto-mode setup skill prompt the model
  reads.
ccVersion: 2.1.207
variables:
  - DATA_AUTO_MODE_DESTRUCTIVE_PERMISSIONS_SECTION_VAR_0
  - DATA_AUTO_MODE_DESTRUCTIVE_PERMISSIONS_SECTION_VAR_1
  - DATA_AUTO_MODE_DESTRUCTIVE_PERMISSIONS_SECTION_VAR_2
  - DATA_AUTO_MODE_DESTRUCTIVE_PERMISSIONS_SECTION_VAR_3
  - DATA_AUTO_MODE_DESTRUCTIVE_PERMISSIONS_SECTION_VAR_4
-->

#### Destructive permissions.allow entries (honored at runtime — auto-approved with no prompt, in your user settings)
${DATA_AUTO_MODE_DESTRUCTIVE_PERMISSIONS_SECTION_VAR_0.map((DATA_AUTO_MODE_DESTRUCTIVE_PERMISSIONS_SECTION_VAR_1)=>`- \`${DATA_AUTO_MODE_DESTRUCTIVE_PERMISSIONS_SECTION_VAR_2(DATA_AUTO_MODE_DESTRUCTIVE_PERMISSIONS_SECTION_VAR_1)}\``).join(`
`)}${DATA_AUTO_MODE_DESTRUCTIVE_PERMISSIONS_SECTION_VAR_3(DATA_AUTO_MODE_DESTRUCTIVE_PERMISSIONS_SECTION_VAR_4)}
