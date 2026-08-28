# Acme FieldOps

Acme FieldOps is a fictional enterprise field-service application and independent benchmark for ArchGauge. The clean application will be fully runnable; deliberately flawed scenarios will remain source-only and will never be publicly deployed.

> Status: foundation only. No field-service workflow is implemented yet. Acme is fictional and represents no real customer, company, deployment, or business outcome.

## Planned workflow

A dispatcher creates and assigns a work order. A technician receives cited repair steps from a service manual. A human approves or rejects the AI proposal before operational state changes. Parts reservations preserve inventory invariants, and signed ERP webhooks are persisted, idempotent, retry-safe, and observable.

## Benchmark scenarios

- Clean
- Flawed
- Remediated
- Insufficient evidence

Expected findings stay outside the submitted public evidence. Only the clean scenario may be deployed.

See [the PRD](docs/PRD.md), [architecture](docs/architecture/overview.md), and [roadmap](docs/roadmap.md).

```bash
bun install --frozen-lockfile
git config core.hooksPath .githooks
git diff --check
git diff --cached --check
git diff --check origin/main...HEAD
actionlint
shellcheck .githooks/pre-commit
```

The seed commit is the only direct-to-`main` exception. Every later change to protected `main` arrives through a pull request, and every commit merged into `main` is signed. Releases use Semantic Versioning and human-readable release notes. The public source is [github.com/strataga/acme-fieldops](https://github.com/strataga/acme-fieldops); no deployment exists yet.

Apache License 2.0. See [LICENSE](LICENSE).
