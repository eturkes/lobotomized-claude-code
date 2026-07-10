<!--
name: Session metadata team skills line
description: >-
  A line of the <session_metadata> block listing team skills, injected as
  user-message text in the usage-nudge classifier model call.
ccVersion: 2.1.206
variables:
  - DATA_SESSION_METADATA_TEAM_SKILLS_VAR_0
  - DATA_SESSION_METADATA_TEAM_SKILLS_VAR_1
-->
teamSkills (used by teammates, count is users): ${DATA_SESSION_METADATA_TEAM_SKILLS_VAR_0.teamSkills.map((DATA_SESSION_METADATA_TEAM_SKILLS_VAR_1)=>`${DATA_SESSION_METADATA_TEAM_SKILLS_VAR_1.name} (${DATA_SESSION_METADATA_TEAM_SKILLS_VAR_1.userCount})`).join(", ")}
