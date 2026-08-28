# Acme FieldOps Agent Guide

Global instructions apply. Acme is fictional, but clean behavior must be production-shaped and runnable.

- Bun commands/workspaces; Node.js 24 LTS production runtime.
- DDD modular monolith with Work Management, Knowledge, AI Assistance, Inventory, ERP Integration, Identity, and Operations contexts.
- Domain invariants live in typed domain code and PostgreSQL constraints/transactions.
- AI output is cited and human-approved before operational state changes.
- ERP webhooks require raw-body signatures, event ledger, idempotency, retries, and replay/out-of-order tests.
- Expected benchmark findings never enter submitted evidence. Vulnerable scenarios are never publicly deployed.
- After the seed, every change to protected `main` arrives through a pull request, and every commit merged into `main` is signed. The required checks, direct-push restrictions, and no-routine-bypass policy are recorded in `docs/governance/github-ruleset.md`.
- Before opening a pull request, run `git diff --check`, `actionlint`, and `shellcheck .githooks/pre-commit`. Code phases also require the project test suite and at least 80% measurable coverage.

Remote, deployment, credentials, provider, billing, and cloud actions require explicit approval.
