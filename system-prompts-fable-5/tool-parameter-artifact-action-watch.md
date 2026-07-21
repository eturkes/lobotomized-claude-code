<!--
name: 'Tool parameter: Artifact action — watch/unwatch/status'
description: >-
  Addendum to the Artifact tool's action parameter describing the watch,
  unwatch, and status actions.
ccVersion: null
-->
 'watch' opens a live-update subscription to the artifact at `url` so this session is notified when another session republishes it; 'unwatch' stops that subscription; 'status' lists this session's artifact watches (pass `url` to check one). Watches live only as long as this session.
