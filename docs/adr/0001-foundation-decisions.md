# ADR 0001: Foundation Decisions

**Status:** Accepted — 2026-08-27

- Apache License 2.0 and a separate repository from ReadyRay.
- Fictional application with no invented customer outcomes.
- DDD modular monolith and clean/hexagonal boundaries.
- Bun commands with Node.js 24 LTS production runtime.
- Human approval before AI proposals affect operational state.
- PostgreSQL transactions/constraints for inventory; transactional outbox and signed idempotent ERP webhooks.
- Clean-only deployment; expected findings stored outside submitted evidence.
- One seed commit, then signed PR-only changes, SemVer, changelog, and release notes.

These decisions maximize benchmark clarity without premature distributed infrastructure.
