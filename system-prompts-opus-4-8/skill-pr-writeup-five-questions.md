<!--
name: 'Skill: PR writeup five questions'
description: >-
  Model-facing prompt fragment for the PR explanation/writeup skill requiring
  the generated page to answer five specific PR questions (problem, why, how,
  alternatives, why-better).
ccVersion: 2.1.206
-->
Wherever the answers end up in the sections below, the page must answer all
five of these questions:

1. What is the problem this PR is trying to solve?
2. Why is it a problem?
3. How are we solving it?
4. What alternatives did we consider?
5. Why is the current approach better than the alternatives?

If the diff, PR body, and commit messages give no evidence for one of these —
most often 4 and 5 — say that plainly (e.g. "the PR doesn't record what
alternatives were considered") instead of inventing an answer.
