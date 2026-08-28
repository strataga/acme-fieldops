# Acme FieldOps Product Requirements

Acme is a fictional, runnable enterprise field-service application used to test architecture-review behavior without inventing customer outcomes.

## Core journey

1. Dispatcher creates a work order and assigns a technician.
2. Technician attaches or selects a service manual.
3. A configured AI provider proposes cited repair steps, hazards, and parts.
4. A human approves or rejects the proposal before operational state changes.
5. Parts reservation and work completion preserve transactional inventory invariants.
6. A signed ERP event is stored and delivered idempotently with retry and replay visibility.

## Benchmark contract

Pin clean, flawed, remediated, and insufficient-evidence commits. Keep the expected-findings oracle outside submitted evidence. Deploy only the clean revision. Label all public examples fictional.

## Quality

WCAG 2.2 AA, OpenAPI 3.1, RFC 9457, complete Postman coverage, server-side authorization, OWASP ASVS-aligned tests, OpenTelemetry, recovery runbooks, at least 80% measurable coverage, SemVer, release notes, SBOMs, signatures, and attestations.

Not yet implemented: every functional item above.
