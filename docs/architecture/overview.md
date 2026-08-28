# Architecture Overview

Acme starts as a modular monolith with web, API, and worker processes around shared domain/application packages.

## Bounded contexts

- Identity and Access
- Work Management
- Knowledge and Manuals
- AI Assistance
- Inventory
- ERP Integration
- Operations

Work orders use an explicit lifecycle. Inventory reservation and completion use database constraints and transactions. AI proposals cite manual evidence and cannot change work-order or inventory state until a permitted human approves them. ERP delivery uses a transactional outbox and durable event ledger so duplicates, retries, and out-of-order messages are safe.

Transport, persistence, AI, storage, and ERP clients are adapters behind ports. Composition roots wire dependencies only. PostgreSQL is canonical; OpenTelemetry correlates user, work-order, AI, inventory, and delivery activity.
