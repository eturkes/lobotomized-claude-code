<!--
name: goal-iterate-until nudge — situation
description: >-
  The "situation" matcher copy for the goal-iterate-until usage nudge, injected
  into the model-facing usage-nudge catalog.
ccVersion: 2.1.206
-->
User says "keep going until X", "don't stop until X", "continue until X", or "loop until X" — they want Claude to persist toward a stated end-state. Also matches when the user has typed "continue" or "keep going" two or more times in the current exchange to nudge Claude past where it stopped. The distinguishing signal is iteration toward a *condition*, not polling a status (that is manual-polling).
