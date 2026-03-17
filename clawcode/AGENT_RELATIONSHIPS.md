# SR2 Agents and Relationships

This document maps all current agents and how they interact in the SR2 factory model.

## Agents

- **orchestrator (El Tano 🧭)**
  - Coordinates all specialists end-to-end.
  - Enforces architecture gate before major implementation.
  - Enforces shift-left QA and Security.

- **lead-architect (🏛️)**
  - Defines boundaries, interfaces, ADRs and NFR tradeoffs.
  - Must approve architecture before significant implementation.

- **product-manager (📦)**
  - Converts strategy/customer needs into executable artifacts.
  - Defines acceptance criteria and outcomes.

- **project-manager (📅)**
  - Drives cadence, dependencies, planning and execution tracking.

- **uxui-dev (🎨)**
  - Creates user flows, IA and implementation-ready UX specs.

- **frontend-dev (🖥️)**
  - Implements UI/UX behavior from approved product + architecture inputs.

- **backend-dev (⚙️)**
  - Implements backend services, APIs and data contracts.

- **fullstack-dev (🛠️)**
  - Implements cross-layer features aligned with ADRs and ACs.

- **qa-dev (✅)**
  - Owns quality strategy, risk-based testing and go/no-go evidence.

- **security-dev (🔐)**
  - Owns proactive security controls and mitigation paths.

- **devops-dev (🚀)**
  - Owns CI/CD, operational reliability, observability and rollback paths.

- **smart-contracts-dev (⛓️)**
  - Owns secure smart contract development, invariants and auditability.

---

## Relationship Graph (Who depends on whom)

## Primary flow
1. **product-manager** defines scope/outcomes + acceptance criteria.
2. **lead-architect** approves architecture/ADRs and boundaries.
3. **orchestrator** assigns execution to the proper specialist(s).
4. **uxui-dev** (if UI scope) delivers implementation-ready design inputs.
5. **frontend-dev / backend-dev / fullstack-dev / smart-contracts-dev** implement.
6. **security-dev** reviews controls and risks (shift-left and pre-release).
7. **qa-dev** validates quality gates and release readiness.
8. **devops-dev** ensures CI/CD and production-safe rollout.
9. **project-manager** tracks status/dependencies/blockers during the entire flow.

## Cross-functional coupling
- **frontend-dev ↔ uxui-dev**: UI implementation fidelity.
- **frontend-dev ↔ backend-dev**: API contract alignment.
- **backend-dev ↔ security-dev**: auth/data protection controls.
- **all implementation roles ↔ qa-dev**: testability and release evidence.
- **all roles ↔ devops-dev**: deployment and operability constraints.
- **orchestrator ↔ all**: assignment, sequencing, risk escalation.

---

## Governance Rules Across Agents

- Reproducible and traceable outputs.
- Respect role boundaries and least-privilege.
- Escalate architectural/security/quality risks early.

---

## Delivery Lifecycle & Gates

- Discovery → Architecture → Implementation → Security/QA → Release → Post-release
- Full gate model and SLA details: `OPERATING_SYSTEM.md`
- Quality/Security thresholds and exceptions: `GATE_POLICY.md`

## Delegation/Handoff Rules (Practical)

When orchestrator delegates, use the mandatory schema in `HANDOFF_CONTRACT.md`.

Minimum required fields:
- objective
- scope / out-of-scope
- acceptance criteria
- dependencies and deadlines
- required artifacts and traceability links

When specialist returns, include:
- result summary
- changed artifacts
- risks/open questions
- verification evidence
