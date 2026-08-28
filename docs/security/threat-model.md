# Foundation Threat Model

Assets: identities, tenant/work-order data, manuals, AI proposals, inventory, ERP credentials/events, audit history, benchmark integrity, and releases.

Trust boundaries: browser/API, tenant/database, uploaded manual/parser, application/model provider, worker/queue, ERP webhook, operator tools, and CI/registry.

Primary abuses: wrong-user or wrong-role access, hostile/manual prompt injection, unsafe attachment, fabricated citation, AI-driven state change, inventory race, webhook forgery/replay, event loss/duplication, benchmark-oracle leakage, vulnerable-scenario deployment, secrets leakage, and supply-chain compromise.

Controls: server authorization matrix, bounded files, secret scanning, cited structured AI output, human approval, PostgreSQL constraints/transactions, signature verification, event ledger/outbox, idempotency, audit logs, clean-only deploy allowlist, least privilege, hostile tests, SBOMs, and signed artifacts. Implementation evidence is pending.
