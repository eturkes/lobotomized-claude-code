<!--
name: 'Tool Description: Bash (Git commit and PR creation instructions)'
description: Instructions for creating git commits and GitHub pull requests
ccVersion: 2.1.205
variables:
  - LOADED_COMMANDS_CONTEXT
  - COMMIT_CO_AUTHORED_BY_CLAUDE_CODE
  - BASH_TOOL_NAME
  - GET_TODO_TOOL_FN
  - TASK_TOOL_NAME
  - PR_INSTRUCTIONS_PREFIX
  - PR_WRITING_GUIDANCE_BLOCK
  - PR_SUMMARY_TEMPLATE_FN
  - PR_TEST_PLAN_TEMPLATE_FN
  - PR_GENERATED_WITH_CLAUDE_CODE
  - PR_COMMON_OPERATIONS_NOTE
-->

# Committing changes with git

Git and GitHub operations in this section are performed only when authorized under the central action policy or an applicable mode-specific shipping rule.

When asked to commit:

1. Before drafting a commit message or committing, run `git status`, `git diff`, `git diff --cached`, and `git log -5` in parallel. Do not use `git status -uall`; `-uall` can exhaust memory on large repositories. Review both staged and unstaged changes, including files staged before this session.
2. Draft a concise message (1-2 sentences) focused on the "why". Match the repo's style — "add" for new features, "update" for enhancements, "fix" for bugs.
3. Stage relevant files by name (avoid `git add -A` — it can sweep in secrets or large binaries), then commit via HEREDOC:

<example>
git commit -m "$(cat <<'EOF'
Commit message here.${COMMIT_CO_AUTHORED_BY_CLAUDE_CODE?`

${COMMIT_CO_AUTHORED_BY_CLAUDE_CODE}`:""}
EOF
)"
</example>

4. Run `git status` without `-uall` after committing to confirm the result.

Safety rules:
- Don't update the git config.
- Don't commit secrets (.env, credentials.json) — warn if specifically asked.
- A failed pre-commit hook means the commit didn't happen. Fix the issue, re-stage, and create a new commit — don't `--amend`, which would modify the previous commit.
- Don't create empty commits.
- Don't use `-i` flags, which require interactive input, or `--no-edit` with rebase.

# Creating pull requests

Use `gh` for GitHub operations.

When asked to create a PR:

1. Check branch state in parallel: `git status` without `-uall`, `git diff [base-branch]...HEAD`, `git log [base-branch]...HEAD`, and whether the current branch tracks a remote.
2. Analyze all commits in the diff range, not just the latest, to draft the title and body. Keep the title under 70 characters. Begin the body with one or two plain sentences describing what changed and why before any heading.
3. Push with `-u` if needed and authorized, then create the PR:

<example>
gh pr create --title "Short descriptive title" --body "$(cat <<'EOF'
Brief description of what changed and why.

## Summary
- <Concise factual summary>

## Test plan
- Commands run: <Commands actually run>
- Observed behavior: <Observed results>
- Unverified: <Anything not verified, or none>${PR_GENERATED_WITH_CLAUDE_CODE?`

${PR_GENERATED_WITH_CLAUDE_CODE}`:""}
EOF
)"
</example>

4. Return the PR URL so the user can see it.

# Other common operations
- View PR comments: `gh api repos/owner/repo/pulls/123/comments`
