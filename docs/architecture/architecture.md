# Architecture

> **Authority:** This file is the authoritative, human-reviewed architecture record.
>
> **State semantics:** Baseline is currently implemented or operating. Transition is approved temporary or intermediate architecture. Target is approved future intent. Implementation alone is not evidence of target intent.

## Source repositories

| Source ID | Repository | Role | Configured ref | Resolved commit |
|---|---|---|---|---|
| SRC-001 | EdgarAlvarez10/CleanArchitecture | primary | main | a6285b9e1b81cdb0d7dbf60a2001be39841b9a5b |

Access mode for this source: local.

## Drivers and constraints

### ARC-DRV-001 — Clean Architecture template for ASP.NET Core and Aspire

Status: baseline

The materialized README states the repository is a Clean Architecture solution template for enterprise application development using ASP.NET Core and Aspire. It also states the template can generate Angular, React, or Web API-only variants, and that the main branch line is on .NET 10.0.

## Solution context

### ARC-CTX-001 — Layered solution template context

Status: baseline

The materialized solution file lists a multi-project solution with AppHost, ServiceDefaults, Application, Domain, Infrastructure, Shared, Web, and test projects. The current checkout is therefore a layered solution template, but the specific generated product variant is unknown from the materialized evidence.

## Components and responsibilities

### ARC-CMP-001 — Solution project layers

Status: baseline

- Responsibility: host, shared service defaults, application, domain, infrastructure, shared support, web entrypoint, and tests as separate solution projects.
- Owning repository: EdgarAlvarez10/CleanArchitecture
- Evidence: README.md and CleanArchitecture.slnx in the materialized evidence set.

## Repository ownership of components

| Component ID | Repository | Ownership |
|---|---|---|
| ARC-CMP-001 | EdgarAlvarez10/CleanArchitecture | Implementation owner |

## Interfaces and integrations

### ARC-INT-001 — Source-level interface surface is unknown

Status: baseline

The materialized evidence exposes the AppHost launch path and Aspire dashboard startup, but it does not expose source-level API contracts, asynchronous message flows, or external integrations. Those interfaces remain unknown in this evidence set.

## Cross-repository relationships

No cross-repository relationships are evidenced in the materialized files.

## Data ownership

### ARC-DATA-001 — Persistence provider choice is unknown

Status: baseline

The materialized package manifest shows central package management for Entity Framework Core, Identity EF Core, and conditional SQLite, PostgreSQL, and SQL Server packages. The selected provider, schema, and ownership of persisted data are unknown from the materialized evidence.

## Security and trust boundaries

### ARC-SEC-001 — Security model is unknown

Status: baseline

The materialized evidence shows support packages related to identity and JWT, but it does not expose source-level authentication, authorization, encryption, or trust-boundary behavior. Those details remain unknown.

## Deployment architecture

### ARC-DEP-001 — AppHost-driven local launch

Status: baseline

The README instructs local execution with `dotnet run --project .\src\AppHost` and states that the Aspire dashboard opens automatically. `global.json` pins SDK 10.0.401, and `Directory.Build.props` targets net10.0.

## Operational architecture

### ARC-OPS-001 — Development environment separation

Status: baseline

The `.devcontainer/README.md` states the dev container configuration is for VS Code Remote Containers or GitHub Codespaces and has no runtime effect. Operational behavior beyond the AppHost/Aspire launch path is not evidenced.

## Baseline architecture

### ARC-BASE-001 — Current implemented state

Status: implemented

The baseline architecture recoverable from the materialized evidence is a .NET 10 Clean Architecture solution template with a layered project structure, central package management, AppHost-based local startup, and an Aspire-oriented developer workflow.

## Transition architecture

### ARC-TRANS-001 — No approved transition currently evidenced

Status: unknown

Do not infer a transition from the current implementation evidence.

## Target architecture

### ARC-TARGET-001 — No approved target currently evidenced

Status: unknown

Do not infer a target from the current implementation evidence.

## Architecture decisions

### ARC-DEC-001 — No approved decision currently evidenced

- Status: proposed
- Context: The materialized evidence set does not expose approved decision records that change the observed baseline.
- Decision: Unknown from the materialized evidence.
- Consequences: Unknown from the materialized evidence.
- Approval evidence: Unknown.

## Contradictions

### ARC-CON-001 — No contradictions evidenced

No contradictions were observed in the materialized evidence set.

## Unknowns

### ARC-UNK-001 — Unresolved baseline questions

The following questions remain unknown from the materialized evidence set:

- Which database provider is selected in this checkout?
- Which generated client framework variant, if any, is present in this checkout?
- What exact source-level endpoints, domain rules, and data models are implemented?
- What are the implemented authentication, authorization, encryption, and trust-boundary behaviors?
- What monitoring, retry, recovery, and failure-handling behavior is implemented at runtime?
