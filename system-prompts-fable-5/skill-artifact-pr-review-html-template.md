<!--
name: 'Skill: Artifact PR-review HTML template'
description: >-
  HTML body-fragment template for the PR-review artifact, with slot markers and
  instructions to the model to HTML-escape untrusted PR-derived input.
ccVersion: null
-->
<!-- Artifact-tool body fragment — no <!DOCTYPE>/<html>/<head>/<body> wrapper. See SKILL.md for slot guidance.
     SECURITY: every string that originates from the PR (title, description, diff lines,
     file paths, comments, author names) is untrusted input. HTML-escape it before it
     lands in any slot: & → &amp;   < → &lt;   > → &gt;   " → &quot;   ' → &#39;.
     Attribute values you author are ALWAYS double-quoted — never single-quoted or bare. -->
<title><!-- SLOT: TAB_TITLE — "PR review: " + the synthesis title, plain text -->PR review</title>
<style>
  /* Design tokens ported from the prototype page's token sheet (warm-gray
     Z/T ramps, extended palette, type scale). Values are hand-copied so the
     page stays self-contained. The dark blocks must mirror any light-block
     additions. */
  :root {
    color-scheme: light;
    --z0: #ffffff;
    --z1: #f6f6f4;
    --t1: hsla(60, 3%, 4%, 0.04);
    --t2: hsla(60, 3%, 4%, 0.06);
    --t3: hsla(60, 3%, 4%, 0.1);
    --t5: hsla(60, 3%, 4%, 0.25);
    --t6: hsla(60, 3%, 4%, 0.5);
    --t7: hsla(60, 3%, 4%, 0.8);
    --t9: hsla(60, 3%, 4%, 1);
    --ink: #141413;
    --ink-soft: #6d6b67;
    --accent: hsla(210, 100%, 45%, 1);
    --accent-10: hsla(210, 100%, 45%, 0.1);
    --ok: hsla(134, 68.1%, 36.9%, 1);
    --ok-10: hsla(134, 68.1%, 36.9%, 0.1);
    --warn: hsla(25, 76%, 44%, 1);
    --warn-10: hsla(25, 76%, 44%, 0.1);
    --bad: hsla(3, 100%, 59.4%, 1);
    --bad-10: hsla(3, 100%, 59.4%, 0.1);
    --sans: "Anthropic Sans", "Styrene B LC", ui-sans-serif, system-ui, -apple-system, "Segoe UI", sans-serif;
    --mono: "Anthropic Mono", "SF Mono", ui-monospace, Menlo, Consolas, monospace;
    font-family: var(--sans);
  }
  @media (prefers-color-scheme: dark) {
    :root:not([data-theme="light"]) {
      color-scheme: dark;
      --z0: #262624;
      --z1: #1b1a17;
      --t1: hsla(50, 9%, 94%, 0.05);
      --t2: hsla(50, 9%, 94%, 0.08);
      --t3: hsla(50, 9%, 94%, 0.13);
      --t5: hsla(50, 9%, 94%, 0.3);
      --t6: hsla(50, 9%, 94%, 0.55);
      --t7: hsla(50, 9%, 94%, 0.85);
      --t9: hsla(50, 9%, 94%, 1);
      --ink: #faf9f5;
      --ink-soft: #b8b5ad;
      --accent: hsla(210, 100%, 62%, 1);
      --accent-10: hsla(210, 100%, 62%, 0.12);
      --ok: hsla(134, 55%, 52%, 1);
      --ok-10: hsla(134, 55%, 52%, 0.12);
      --warn: hsla(25, 85%, 58%, 1);
      --warn-10: hsla(25, 85%, 58%, 0.12);
      --bad: hsla(3, 100%, 68%, 1);
      --bad-10: hsla(3, 100%, 68%, 0.12);
    }
  }
  :root[data-theme="dark"] {
    color-scheme: dark;
    --z0: #262624;
    --z1: #1b1a17;
    --t1: hsla(50, 9%, 94%, 0.05);
    --t2: hsla(50, 9%, 94%, 0.08);
    --t3: hsla(50, 9%, 94%, 0.13);
    --t5: hsla(50, 9%, 94%, 0.3);
    --t6: hsla(50, 9%, 94%, 0.55);
    --t7: hsla(50, 9%, 94%, 0.85);
    --t9: hsla(50, 9%, 94%, 1);
    --ink: #faf9f5;
    --ink-soft: #b8b5ad;
    --accent: hsla(210, 100%, 62%, 1);
    --accent-10: hsla(210, 100%, 62%, 0.12);
    --ok: hsla(134, 55%, 52%, 1);
    --ok-10: hsla(134, 55%, 52%, 0.12);
    --warn: hsla(25, 85%, 58%, 1);
    --warn-10: hsla(25, 85%, 58%, 0.12);
    --bad: hsla(3, 100%, 68%, 1);
    --bad-10: hsla(3, 100%, 68%, 0.12);
  }
  * { box-sizing: border-box; }
  body { margin: 0; background: var(--z1); color: var(--ink); font-size: 13px; line-height: 18px; -webkit-font-smoothing: antialiased; }
  .page { padding: 24px 24px 56px; display: flex; flex-direction: column; align-items: center; }
  .window { width: 100%; max-width: 1200px; background: var(--z0); border-radius: 16px; box-shadow: 0 0 0 1px var(--t2), 0 6px 16px 0 hsla(60, 3%, 4%, 0.06); }

  .topbar { display: flex; align-items: center; gap: 8px; padding: 12px 12px 10px 12px; border-bottom: 1px solid var(--t2); }
  .brand { font-weight: 500; font-size: 13px; white-space: nowrap; margin-left: 2px; }
  .crumb { font-size: 12px; line-height: 15px; color: var(--t6); }
  .topbar .gh { margin-left: auto; font-size: 12px; color: var(--accent); text-decoration: underline; text-underline-offset: 2px; }

  /* Staleness banner: hidden until the baked script (bottom of this file) learns the PR
     head moved since publish. Its copy is fixed here in the template — never filled from
     PR content. */
  .stale-banner { padding: 9px 14px; border-bottom: 1px solid var(--t2); border-left: 3px solid var(--warn); background: var(--warn-10); color: var(--ink); font-size: 12px; line-height: 17px; }
  .stale-banner .lead { color: var(--ink); font-weight: 600; }
  .stale-banner code { font-family: var(--mono); font-size: 0.92em; background: var(--t1); border-radius: 3px; padding: 0 3px; }

  main { max-width: 720px; width: 100%; margin: 0 auto; padding: 32px 30px 24px; display: flex; flex-direction: column; gap: 44px; }
  main > section { margin: 0; }

  .byline { display: flex; align-items: center; gap: 9px; font-size: 12px; line-height: 15px; color: var(--t6); flex-wrap: wrap; }
  .byline .spark { width: 18px; height: 18px; flex-shrink: 0; display: grid; place-items: center; background: var(--warn-10); border-radius: 5px; color: var(--warn); }
  .byline .who { color: var(--ink); font-weight: 500; }
  .byline .ref { margin-left: auto; font-family: var(--mono); font-size: 12px; color: var(--t5); }

  h1.title { margin: 10px 0 0; font-size: 22px; line-height: 28px; font-weight: 600; letter-spacing: -0.01em; color: var(--ink); text-wrap: pretty; }

  .chips { display: flex; align-items: center; gap: 6px; margin-top: 12px; flex-wrap: wrap; }
  .chip { display: inline-flex; align-items: center; height: 16px; padding: 0 4px; border-radius: 4px; font-size: 12px; line-height: 15px; font-weight: 500; white-space: nowrap; background: var(--t2); color: var(--t7); }
  .chip.ok     { background: var(--ok-10);     color: var(--ok); }
  .chip.warn   { background: var(--warn-10);   color: var(--warn); }
  .chip.bad    { background: var(--bad-10);    color: var(--bad); }
  .chip.accent { background: var(--accent-10); color: var(--accent); }
  .chips-note { font-size: 11px; line-height: 13px; color: var(--t5); }

  .bottom-line { margin: 14px 0 0; font-size: 15.5px; line-height: 26px; color: var(--ink); text-wrap: pretty; border-left: 2px solid var(--t2); padding-left: 18px; }
  .bottom-line code, code.chip-code { font-family: var(--mono); font-size: 0.92em; background: var(--t1); border-radius: 3px; padding: 0 3px; }

  figure.visual { margin: 18px 0 0 18px; }
  figure.visual figcaption { font-size: 11px; line-height: 13px; color: var(--t6); margin-top: 8px; }
  .diagram { background: var(--t1); border-radius: 8px; padding: 16px; overflow-x: auto; }
  .diagram svg { display: block; max-width: 100%; height: auto; }

  /* Flow block: vertical timeline. Marker hue per step: .new → accent, .changed → warn, .unchanged → faint. */
  ol.flow { list-style: none; margin: 0; padding: 0; }
  ol.flow li { display: flex; gap: 8px; }
  ol.flow .rail { display: flex; flex-direction: column; align-items: center; width: 9px; flex-shrink: 0; }
  ol.flow .dot { width: 9px; height: 9px; margin-top: 3px; border-radius: 999px; background: var(--t5); }
  ol.flow li.changed .dot { background: var(--warn); box-shadow: 0 0 0 3px var(--warn-10); }
  ol.flow li.new .dot { background: var(--accent); box-shadow: 0 0 0 3px var(--accent-10); }
  ol.flow .stem { width: 1px; flex: 1; min-height: 10px; background: var(--t3); }
  ol.flow li:last-child .stem { display: none; }
  ol.flow .step-body { padding-bottom: 10px; min-width: 0; display: flex; flex-direction: column; gap: 1px; }
  ol.flow .step-label { font-size: 12px; line-height: 15px; font-weight: 500; color: var(--ink); display: inline-flex; align-items: center; gap: 6px; flex-wrap: wrap; }
  ol.flow .step-label .chip { height: 12px; border-radius: 3px; font-size: 11px; line-height: 13px; text-transform: uppercase; }
  ol.flow .step-detail { display: block; font-size: 12px; line-height: 15px; color: var(--ink-soft); }
  ol.flow .step-was { display: block; font-size: 11px; line-height: 13px; color: var(--t6); }

  /* Before/after panels */
  .ba { display: grid; grid-template-columns: 1fr 1fr; gap: 12px; }
  .ba .panel { background: var(--z0); box-shadow: inset 0 0 0 1px var(--t2); border-radius: 8px; padding: 12px 14px; }
  .ba h4 { margin: 0 0 8px; font-size: 11px; line-height: 13px; text-transform: uppercase; letter-spacing: 0.06em; font-weight: 600; color: var(--t6); }
  .ba ul { margin: 0; padding: 0; list-style: none; }
  .ba li { font-size: 13px; line-height: 18px; padding: 3px 0; }
  .ba li.good::before { content: "●"; color: var(--ok); margin-right: 7px; font-size: 9px; vertical-align: 1px; }
  .ba li.bad::before { content: "●"; color: var(--bad); margin-right: 7px; font-size: 9px; vertical-align: 1px; }
  .ba li.neutral::before { content: "●"; color: var(--t5); margin-right: 7px; font-size: 9px; vertical-align: 1px; }

  .your-call { margin: 0; }
  .your-call > h2 { margin: 0 0 14px; font-size: 11px; line-height: 13px; font-weight: 600; letter-spacing: 0.06em; text-transform: uppercase; color: var(--t6); }
  .call-item { display: grid; grid-template-columns: 14px 1fr; gap: 12px; padding-left: 2px; }
  .call-item + .call-item { margin-top: 22px; }
  .call-item .marker { color: var(--warn); font-size: 13px; line-height: 21px; }
  .call-item p { margin: 0; font-size: 13.5px; line-height: 21px; color: var(--t7); text-wrap: pretty; }
  .call-item .q { color: var(--ink); font-weight: 500; }
  .call-item .lean { margin: 8px 0 0; font-size: 12px; line-height: 18px; color: var(--t6); }
  .anchor-snippet { display: block; font-family: var(--mono); font-size: 12px; line-height: 17px; color: var(--t6); white-space: nowrap; overflow: hidden; text-overflow: ellipsis; max-width: 100%; margin-top: 4px; }
  .pills { display: flex; flex-wrap: wrap; gap: 6px; margin-top: 10px; }
  .pill { display: inline-flex; align-items: center; height: 22px; padding: 0 10px; border-radius: 5px; font-size: 12px; background: var(--z0); color: var(--t7); box-shadow: inset 0 0 0 1px var(--t3); opacity: 0.7; cursor: default; }

  .actions { margin: 0; }
  .actions .gh-btn { display: inline-flex; align-items: center; justify-content: center; gap: 6px; height: 34px; padding: 0 16px; border-radius: 8px; font-size: 13.5px; font-weight: 500; color: var(--t6); text-decoration: none; background: transparent; box-shadow: inset 0 0 0 1px var(--t3); }
  .actions .note { margin: 8px 0 0; font-size: 11px; line-height: 14px; color: var(--t5); padding-left: 2px; }

  .followups { margin: 0; }
  .followups h2 { margin: 0 0 6px; font-size: 11px; line-height: 13px; font-weight: 600; text-transform: uppercase; letter-spacing: 0.06em; color: var(--t6); }
  .followups ul { margin: 0 2px; padding-left: 16px; }
  .followups li { font-size: 12px; line-height: 18px; color: var(--t7); padding: 1px 0; }

  details.more { border-top: 1px solid var(--t2); padding-top: 18px; }
  details.more > summary { list-style: none; cursor: pointer; display: flex; align-items: center; gap: 8px; font-size: 13px; color: var(--t7); }
  details.more > summary::-webkit-details-marker { display: none; }
  details.more > summary::before { content: "›"; color: var(--t5); display: inline-block; width: 8px; transition: transform 0.15s ease; }
  details.more[open] > summary::before { transform: rotate(90deg); }
  details.more > summary .sum-meta { font-weight: 400; color: var(--t5); font-size: 12px; }
  .more-body { display: flex; flex-direction: column; gap: 18px; padding: 18px 0 4px 16px; font-size: 12px; line-height: 18px; color: var(--ink-soft); }
  .more-body h3 { margin: 0 0 6px; font-size: 12px; font-weight: 600; color: var(--ink); }

  .signal-grid { display: grid; grid-template-columns: auto 1fr; gap: 6px 14px; align-items: baseline; font-size: 12px; line-height: 18px; }
  .signal-grid .k { color: var(--accent); font-weight: 500; }

  .file-row { display: grid; grid-template-columns: 12px 1fr auto; gap: 10px; font-family: var(--mono); font-size: 12px; line-height: 17px; padding: 4px 0; border-bottom: 1px solid var(--t2); align-items: baseline; }
  .file-row:last-child { border-bottom: 0; }
  .file-row .mode { font-weight: 600; color: var(--warn); }
  .file-row .mode.add { color: var(--ok); }
  .file-row .mode.del { color: var(--bad); }
  .file-row .mode.ren { color: var(--t6); }
  .file-row .delta { white-space: nowrap; }
  .file-row .plus { color: var(--ok); }
  .file-row .minus { color: var(--bad); }

  .explainer { background: var(--t1); border-radius: 8px; padding: 8px 12px 12px; }
  .explainer .headline { font-size: 12px; line-height: 18px; margin: 6px 0 12px; color: var(--ink-soft); }
  .explainer .headline strong { font-weight: 500; color: var(--ink); }
  .explainer-blocks { display: flex; flex-direction: column; gap: 16px; }
  .explainer-blocks figure.visual { margin-left: 0; }
  details.concern { border-top: 1px solid var(--t2); padding-top: 10px; }
  details.concern > summary { list-style: none; cursor: pointer; font-size: 12px; line-height: 18px; font-weight: 500; color: var(--ink); display: flex; gap: 6px; }
  details.concern > summary::-webkit-details-marker { display: none; }
  details.concern > summary::before { content: "›"; color: var(--t5); flex-shrink: 0; width: 8px; transition: transform 0.15s ease; }
  details.concern[open] > summary::before { transform: rotate(90deg); }
  details.concern p { font-size: 12px; line-height: 18px; color: var(--ink-soft); margin: 8px 0 0 16px; text-wrap: pretty; }

  .blind-spots { border-top: 1px solid var(--t2); padding-top: 10px; font-size: 11px; line-height: 16px; color: var(--t6); margin: 0; }

  .lede-foot { margin: 0; font-size: 11px; line-height: 16px; color: var(--t5); }

  @media (max-width: 760px) {
    main { padding: 28px 8px 20px; gap: 36px; }
    h1.title { font-size: 20px; line-height: 26px; }
    .bottom-line { padding-left: 14px; font-size: 15px; line-height: 24px; }
    .ba { grid-template-columns: 1fr; }
    .byline .ref { display: none; }
  }
</style>

<div class="page">
  <div class="window">

    <div class="topbar">
      <span class="brand">Claude Code</span>
      <span class="crumb">Review / <!-- SLOT: REPO — "owner/repo", escaped -->owner/repo</span>
      <a class="gh" href="https://github.com/owner/repo/pull/1" target="_blank" rel="noopener noreferrer"><!-- SLOT: GH_LINK — set href to the PR's GitHub URL (also used once more below, on the Review on GitHub button) -->GitHub</a>
    </div>

    <!-- Staleness banner: fixed copy, hidden by default. Only the baked script at the end
         of this template toggles its hidden flag. Not a slot — never edit or fill it. -->
    <div class="stale-banner" role="status" hidden><span class="lead">This page is out of date.</span> The pull request's branch has changed since this page was written. The author can refresh it by re-running <code>/artifact-pr-review</code>.</div>

    <main>
      <section>
        <div class="byline">
          <span class="spark" aria-hidden="true"><svg width="11" height="11" viewBox="0 0 16 16" fill="currentColor"><path d="M8 0l1.6 5.2L15 4l-3.6 4L15 12l-5.4-1.2L8 16l-1.6-5.2L1 12l3.6-4L1 4l5.4 1.2z"/></svg></span>
          <span><span class="who">Claude</span> read <!-- SLOT: ACTIONS_READ — join synthesis.actions_read with ", " (last joined with " and ") -->the PR description, the diff and changed files</span>
          <span class="ref"><!-- SLOT: PR_REF — "repo#N", escaped -->repo#1</span>
        </div>

        <h1 class="title"><!-- SLOT: TITLE — synthesis.title, escaped. Also mirror into TAB_TITLE above. -->Plain-English description of what this PR does</h1>

        <div class="chips">
          <!-- SLOT: CHIPS — one class chip (the change class you inferred, neutral styling)
               and one recommendation chip rendering synthesis.recommendation from the generated
               JSON — class AND display text: approve → class "chip ok", text "approve";
               approve_once_resolved → class "chip warn", text "approve once resolved";
               request_changes → class "chip bad", text "request changes" (spaces, never the
               raw snake_case token). Keep to these two chips, and keep the inferred-note
               span that follows them: nothing on this page is computed by a backend, and the
               reader must be able to see that. -->
          <span class="chip">mechanical</span>
          <span class="chip ok">approve</span>
          <span class="chips-note">inferred by Claude — not a computed status</span>
        </div>

        <p class="bottom-line"><!-- SLOT: BOTTOM_LINE — synthesis.bottom_line, escaped; wrap identifier-like
             tokens you would say in monospace in <code> (that markup is yours, not the PR's). -->Three to five sentences on what the PR changes, why, and how — written for someone who has not read the diff.</p>

        <!-- SLOT: SYN_VISUAL — synthesis.visual rendered as ONE of the three block shapes
             (flow timeline / delta diagram / before-after panels; markup patterns are in the
             explainer section below — reuse them here). DELETE this whole figure when
             synthesis.visual is null. -->
        <figure class="visual">
          <ol class="flow">
            <li class="changed">
              <span class="rail" aria-hidden="true"><span class="dot"></span><span class="stem"></span></span>
              <span class="step-body">
                <span class="step-label">First pipeline step <span class="chip warn">changed</span></span>
                <span class="step-detail">What this step does now.</span>
                <span class="step-was">was: what it did before</span>
              </span>
            </li>
            <li class="unchanged">
              <span class="rail" aria-hidden="true"><span class="dot"></span><span class="stem"></span></span>
              <span class="step-body">
                <span class="step-label">Second pipeline step</span>
                <span class="step-detail">Unchanged context step.</span>
              </span>
            </li>
          </ol>
          <figcaption>One-line caption for the visual.</figcaption>
        </figure>
      </section>

      <!-- SLOT: YOUR_CALL — one .call-item per synthesis.concerns entry. DELETE the whole
           section when concerns is empty (zero is the common case). Update the count in the h2.
           Pills: one per option, plus a final "Skip" pill; all are inert spans styled as pills.
           When a concern has an anchor, append to its context paragraph:
           <code class="chip-code">{anchor.file, escaped}:{anchor.line}</code> (omit the
           ":{anchor.line}" part when line is null), then on its own line
           <span class="anchor-snippet">{anchor.snippet, escaped}</span>.
           Both render as escaped TEXT CONTENT — the snippet is a verbatim attacker-authored
           diff line and must never land in an attribute value. -->
      <section class="your-call">
        <h2>Needs your call · 1</h2>
        <div class="call-item">
          <span class="marker" aria-hidden="true">●</span>
          <div>
            <p><span class="q">The bolded question a reviewer should weigh?</span> Context for the question — why it is worth the reviewer's attention.</p>
            <p class="lean">Claude leans: the one-line recommended answer.</p>
            <div class="pills">
              <span class="pill" role="button" aria-disabled="true" title="Not wired up in this version">Option one</span>
              <span class="pill" role="button" aria-disabled="true" title="Not wired up in this version">Option two</span>
              <span class="pill" role="button" aria-disabled="true" title="Not wired up in this version">Skip</span>
            </div>
          </div>
        </div>
      </section>

      <section class="actions">
        <a class="gh-btn" href="https://github.com/owner/repo/pull/1" target="_blank" rel="noopener noreferrer">Review on GitHub ↗</a>
        <p class="note">This page is read-only — approve and comment on GitHub.</p>
      </section>

      <section class="followups">
        <h2>Likely follow-ups</h2>
        <ul>
          <!-- SLOT: FOLLOWUPS — one <li> per synthesis.followups item, escaped. -->
          <li>a short lowercase question the reviewer is likely to ask next?</li>
        </ul>
      </section>

      <details class="more">
        <summary>Details<span class="sum-meta"><!-- SLOT: SUM_META — "N signals · N files"; the file count is the PR's total changed files, not the capped row count -->2 signals · 3 files</span></summary>
        <div class="more-body">

          <div>
            <h3>Signals</h3>
            <div class="signal-grid">
              <!-- SLOT: SIGNALS — one k/v row per signal observed via gh (CI status, review
                   decision, mergeability, bot reviews), plus a Coverage row when the diff was
                   only partially read (that one states your own coverage). Values are statements
                   of what you saw, escaped; omit rows you could not observe rather than guessing. -->
              <span class="k">CI</span><span>12/12 checks passing @ abc1234</span>
              <span class="k">Reviews</span><span>no human review yet</span>
            </div>
          </div>

          <div>
            <h3>Files</h3>
            <!-- SLOT: FILES — one .file-row per changed file (cap at 20; add a final
                 "… and N more" plain row beyond that). Mode letter from the files
                 endpoint's status field (step 1) or the diff you actually read:
                 modified/changed → M, added/copied → A (class "mode add"),
                 removed → D (class "mode del"), renamed → R (class "mode ren").
                 When the change type wasn't observed, leave the mode span EMPTY
                 rather than guessing. Paths escaped. -->
            <div class="file-row"><span class="mode">M</span><span>src/example/path.ts</span><span class="delta"><span class="plus">+10</span> <span class="minus">−2</span></span></div>
          </div>

          <div class="explainer">
            <p class="headline"><strong>Visual explainer.</strong> <!-- SLOT: EXPLAINER_HEADLINE — explainer.headline, escaped -->One complete-thought sentence a reviewer reads without expanding anything.</p>
            <div class="explainer-blocks">

              <!-- SLOT: EXPLAINER_BLOCKS — render explainer.blocks in order, one element per
                   block, using these four markup patterns. Delete the sample blocks below.

                   delta_diagram (at most one): ONE inline <svg> with a fixed viewBox and no
                   width/height, wrapped in <figure class="visual"><div class="diagram">…</div>
                   <figcaption>caption</figcaption></figure>. Draw the DELTA, not the final
                   state: boxes for nodes (rounded <rect> + <text>), arrows for edges
                   (<path> + marker or plain line+polygon). Color by kind, via style attributes
                   only (var() fails silently in bare SVG attributes): new → var(--accent),
                   modified → var(--warn), existing → var(--t5) at opacity 0.5. Label
                   edges with small text. 14–16px text, generous padding — cramped diagrams are
                   the most common failure. role="img" + aria-label on the svg; the aria-label
                   is written in your own words, never copied PR text (see the untrusted-input
                   rules — PR-derived strings never go in attributes).

                   flow: the ol.flow timeline pattern (see SYN_VISUAL sample above), wrapped in
                   figure.visual with a figcaption. Step marker class: new | changed | unchanged;
                   label chip matches the marker — new → <span class="chip accent">new</span>,
                   changed → <span class="chip warn">changed</span>, unchanged → no chip;
                   "annotation" goes in .step-was.

                   before_after: <figure class="visual"><div class="ba">
                     <div class="panel"><h4>Before</h4><ul><li class="bad|neutral|good">item</li>…</ul></div>
                     <div class="panel"><h4>After</h4><ul>…</ul></div>
                   </div><figcaption>what flipped</figcaption></figure>

                   concern: the details.concern pattern below, one per concern block, summary =
                   the complete-thought summary, body paragraphs inside. -->
              <details class="concern">
                <summary>A complete-thought concern summary the reader understands without expanding.</summary>
                <p>Mechanism and trade-offs, paragraph one.</p>
              </details>

            </div>
            <p class="blind-spots" style="margin-top: 16px;"><!-- SLOT: BLIND_SPOTS — "Didn't change: " + blind_spots.didnt_change items joined with " · ", escaped. DELETE this <p> when the list is empty. -->Didn't change: adjacent thing one · adjacent thing two</p>
          </div>

        </div>
      </details>

      <p class="lede-foot"><!-- SLOT: LEDE — the top-level lede sentence, escaped -->One sentence: what this PR does and why.</p>
    </main>

  </div>
</div>

<!-- STALENESS ANCHOR (publish-time data island). Fill ONLY the values, per SKILL.md § Step 3b:
     owner, repo, number, headSha (40 lowercase hex), publishedAt (UTC ISO-8601). Leave "live"
     as null unless the GitHub-connector gate in § Step 3b passed; a null "live" makes the page
     render exactly as the static briefing. Values here are validated identifier fields —
     never PR title, description, or diff text.
     Cross-lane contract: "kind", "owner", "repo", "number", and "publishedAt" are the fields every
     review-artifact anchor shares; each "kind" adds its own version field ("pr" → "headSha";
     other kinds add their own) and ships its own baked staleness script with its own hash pin. The script below watches only kind "pr" and
     ignores any other kind, so sibling kinds never edit this block. -->
<script type="application/json" id="prr-anchor">{"anchor":{"kind":"pr","owner":"owner","repo":"repo","number":1,"headSha":"0000000000000000000000000000000000000000","publishedAt":"1970-01-01T00:00:00Z"},"live":null}</script>

<!-- STALENESS SCRIPT — FIXED, VETTED CODE. Copy byte-for-byte; never edit, reorder, or extend
     it. A test pins this block by exact hash, so any change is a deliberate, reviewed hash
     update in the same change. It reads only the #prr-anchor island above and
     the viewer's GitHub connector via window.claude.mcp, and the only thing it can ever change
     is the hidden flag of the .stale-banner element (fixed copy).
     Contract: written against the artifact viewer's runtime MCP surface (window.claude.mcp
     listTools/watchTool, ToolInfo.annotations.readOnlyHint, result.payload, McpError codes);
     the exact contract version is recorded next to the hash pin in the test suite. A change to
     that surface requires editing this block and re-deriving its pinned hash together;
     published pages keep the block they shipped with and fall back to the static page on any
     mismatch. -->
<script>
(function prReviewStaleness() {
  var island = document.getElementById('prr-anchor');
  var banner = document.querySelector('.stale-banner');
  if (!island || !banner) return;

  var cfg;
  try {
    cfg = JSON.parse(island.textContent || 'null');
  } catch (e) {
    return;
  }
  if (!cfg || typeof cfg !== 'object') return;
  var anchor = cfg.anchor;
  var live = cfg.live;

  var HEX40 = /^[0-9a-f]{40}$/i;
  var IDENT = /^[A-Za-z0-9_.-]{1,64}$/;
  var KEY = /^[A-Za-z0-9_]{1,48}$/;

  if (!anchor || anchor.kind !== 'pr') return;
  if (typeof anchor.headSha !== 'string' || !HEX40.test(anchor.headSha)) return;
  if (!live || typeof live !== 'object' || Array.isArray(live)) return;
  if (typeof live.tool !== 'string' || !IDENT.test(live.tool)) return;
  var input = live.input;
  if (!input || typeof input !== 'object' || Array.isArray(input)) return;
  var inputKeys = Object.keys(input);
  if (inputKeys.length > 8) return;
  for (var k = 0; k < inputKeys.length; k++) {
    if (!KEY.test(inputKeys[k])) return;
    var val = input[inputKeys[k]];
    if (typeof val === 'string') {
      if (!IDENT.test(val)) return;
    } else if (typeof val === 'number') {
      if (!Number.isSafeInteger(val)) return;
    } else {
      return;
    }
  }
  var path = live.shaPath;
  if (!Array.isArray(path) || path.length === 0 || path.length > 6) return;
  for (var p = 0; p < path.length; p++) {
    if (typeof path[p] !== 'string' || !KEY.test(path[p])) return;
  }

  /* Bind the watch to the anchored pull request: the live call's input must carry the
     anchor's owner, repo, and number as DISTINCT entries, or the page stays static.
     Distinct-entry consumption (not membership): when owner === repo (grafana/grafana),
     one value must not satisfy both probes — each anchor part consumes its own entry. */
  var OWNER = /^[A-Za-z0-9-]{1,39}$/;
  if (typeof anchor.owner !== 'string' || !OWNER.test(anchor.owner)) return;
  if (typeof anchor.repo !== 'string' || !IDENT.test(anchor.repo)) return;
  if (!Number.isSafeInteger(anchor.number) || anchor.number < 1) return;
  var inputValues = [];
  for (var vk = 0; vk < inputKeys.length; vk++) inputValues.push(input[inputKeys[vk]]);
  var need = [anchor.owner, anchor.repo, anchor.number];
  var used = [];
  for (var nd = 0; nd < need.length; nd++) {
    var foundAt = -1;
    for (var iv = 0; iv < inputValues.length; iv++) {
      if (!used[iv] && inputValues[iv] === need[nd]) { foundAt = iv; break; }
    }
    if (foundAt === -1) return;
    used[foundAt] = true;
  }

  var mcp = window.claude ? window.claude.mcp : undefined;
  if (!mcp || typeof mcp.listTools !== 'function' || typeof mcp.watchTool !== 'function') return;

  var anchorSha = anchor.headSha.toLowerCase();

  /* true = head moved (stale), false = head matches, null = payload shape not understood. */
  function staleVerdict(payload) {
    var cur = payload;
    for (var i = 0; i < path.length; i++) {
      if (!cur || typeof cur !== 'object') return null;
      cur = cur[path[i]];
    }
    if (typeof cur !== 'string' || !HEX40.test(cur)) return null;
    return cur.toLowerCase() !== anchorSha;
  }

  /* A watched tool must be a wire-declared read: the connector itself must
     annotate it readOnlyHint: true. Name-based trust is not enough — an
     unannotated write tool must never be bound to a refetching watch. */
  function isDeclaredRead(tool) {
    var notes = tool ? tool.annotations : null;
    return notes ? notes.readOnlyHint === true : false;
  }

  mcp.listTools().then(function (res) {
    var servers = (res ? res.servers : null) || [];
    var server = null;
    var matches = 0;
    for (var s = 0; s < servers.length; s++) {
      var tools = (servers[s] ? servers[s].tools : null) || [];
      for (var t = 0; t < tools.length; t++) {
        var candidate = tools[t];
        if (candidate ? candidate.name === live.tool : false) {
          if (!isDeclaredRead(candidate)) return;
          server = servers[s].server;
          matches++;
          break;
        }
      }
    }
    if (matches !== 1 || typeof server !== 'string') return;

    var denied = false;
    var stop = mcp.watchTool(
      server,
      live.tool,
      input,
      function (ev) {
        if (!ev) return;
        if (ev.type === 'data') {
          var result = ev.result || {};
          var verdict = staleVerdict(result.payload);
          if (verdict === true) banner.hidden = false;
          else if (verdict === false) banner.hidden = true;
          return;
        }
        if (ev.type === 'error') {
          var code = ev.error ? ev.error.code : undefined;
          switch (code) {
            case 'needs_reauth':
            case 'server_not_connected':
            case 'blocked_by_policy':
            case 'approval_required':
            case 'not_in_manifest':
            case 'not_granted':
            case 'capability_disabled':
            case 'capability_removed':
            case 'selection_required':
            case 'server_not_found':
              banner.hidden = true;
              denied = true;
              if (typeof stop === 'function') { stop(); stop = null; }
              return;
            default:
              return;
          }
        }
      },
      { refetchInterval: 120000, cache: { staleTime: 60000 } }
    );
    /* A denial delivered synchronously during watchTool() runs before \`stop\`
       exists; the flag carries that cancel across the assignment. Nulling
       after every stop() makes the cancel single-shot even if the runtime
       delivers another denial to an already-dead watch. */
    if (denied && typeof stop === 'function') { stop(); stop = null; }
  }).catch(function () {
    return;
  });
})();
</script>
