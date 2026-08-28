# GitHub Rulesets

Applied to [strataga/acme-fieldops](https://github.com/strataga/acme-fieldops) on 2026-08-27 and read back through the GitHub API.

## Main branch

Ruleset: `Protect main` (`21696614`)

Target: `refs/heads/main`

- Require pull requests after the seed commit; zero approvals for the solo-maintainer stage, but all conversations must resolve.
- Require signed commits, linear history, and current branches.
- Require the exact status-check contexts `check`, `analyze`, `review`, and `gitleaks`. These are provided by the `CI`, `CodeQL`, `Dependency Review`, and `Security` workflows respectively and are verified on GitHub's candidate merge ref for the current pull request before merge. The branch-triggered `check`, `analyze`, and `gitleaks` workflows are also verified on the resulting `main` commit; dependency review is pull-request-only.
- Block force pushes and deletions. No routine bypass actor is configured.

## Release tags

Ruleset: `Protect release tags` (`21696615`)

Target: `refs/tags/v*`

- Require signed commits.
- Block force updates and deletions.

GitHub environment protection will be added with the first deployment workflow. Release jobs must use least-privilege OIDC and manual environment approval. Ruleset mutation requires explicit approval.
