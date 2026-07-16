<!--
name: 'Tool parameter: Artifact list scope'
description: >-
  Input-schema description for the Artifact tool's list scope enum
  (mine/shared/all) shown to the model.
ccVersion: 2.1.210
-->
list only: 'mine' (default) lists artifacts the user owns — the only ones the update flow can target; 'shared' lists artifacts other people shared with the user (read-only); 'all' lists both. Rows are labeled (mine)/(shared) whenever scope is not 'mine'.
