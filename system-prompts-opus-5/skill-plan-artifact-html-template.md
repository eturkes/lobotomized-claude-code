<!--
name: 'Skill: plan-artifact HTML template'
description: >-
  Bundled templates/artifact-plan.html shell for the plan-artifact skill
  (registered as SKILL_FILES + PLAN_TEMPLATE) - the title/eyebrow/summary +
  section-run HTML/CSS scaffold the SKILL.md tells the model to copy and fill by
  hand, and that the auto-publish path fills mechanically.
ccVersion: null
fill contract: >-
  the automatic publish path (src/frame/planArtifactHtml.ts) fills this
  mechanically — {{TITLE}}, {{EYEBROW}}, and {{SUMMARY}} are replaced by a fixed
  regex, and everything from the first <section> through the LAST </section> is
  replaced wholesale by the rendered plan body. Keep those three slots and the
  section run, and put nothing after the last </section> except </article>;
  tests in test/frame/planArtifactHtml.test.ts assert this shape.
style: >-
  colors and spacing mirror @ant/cds tokens (comfortable density) as literals —
  a published artifact is standalone, so it cannot import the package.
  Typography is deliberately a plain system stack — no Anthropic brand fonts and
  no serif voice (owner + brand call, thread ts 1782852395) — and the light
  background is white rather than the CDS cream surface-0; those are the
  deliberate deviations from CDS values. Dark mode keys off prefers-color-scheme
  (the standalone equivalent of CDS data-mode).
-->
