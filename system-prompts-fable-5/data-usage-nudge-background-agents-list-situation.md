<!--
name: Background agents list situation
description: >-
  The situation string of the "background-agents-list" usage-nudge object,
  injected into model context as part of the usage-nudge catalog.
ccVersion: 2.1.206
-->
User mentions juggling many Claude sessions in parallel — "I have a bunch of tabs open", "running several of these at once", "lost track of which one", "this one can keep going while I do X", or says they will step away and check back on this session later. Also match when the user asks "which session was working on X?", "was this the tab where we did PR #N?", "where did we fix the Y bug?" — they are trying to recall what a session was about by asking inside it, which means they have lost the overview across sessions. The friction is overseeing many sessions, not coordinating between two of them (that is cross-session-coordination). Also match when the user kicks off long autonomous work and says "I'll come back to this" — they are treating the session as fire-and-forget.
