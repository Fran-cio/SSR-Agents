# SR2 Factory Operating System (v1)

## Objective
Provide an enforceable, measurable operating model for multi-agent software delivery.

## Delivery Lifecycle and Gates

### Phase 1 — Discovery
- **Owner (DRI):** product-manager
- **Entry:** request/problem statement exists
- **Exit:** scope, outcomes, and testable acceptance criteria defined
- **Blockers:** missing stakeholder objective, contradictory requirements
- **Evidence:** story brief, AC list, risk notes
- **Waiver authority:** orchestrator + product-manager

### Phase 2 — Architecture
- **Owner (DRI):** lead-architect
- **Entry:** Discovery outputs approved
- **Exit:** architecture decision approved, boundaries and contracts explicit
- **Blockers:** unresolved data ownership, interface ambiguity, NFR gaps
- **Evidence:** ADR / architecture summary + interface contracts
- **Waiver authority:** lead-architect

### Phase 3 — Implementation
- **Owner (DRI):** frontend-dev / backend-dev / fullstack-dev / smart-contracts-dev
- **Entry:** architecture gate passed
- **Exit:** implementation complete against AC
- **Blockers:** failing CI, unresolved dependencies, missing test assets
- **Evidence:** PR(s), tests, implementation notes
- **Waiver authority:** orchestrator (non-security, non-architecture only)

### Phase 4 — Security & QA Validation
- **Owner (DRI):** security-dev + qa-dev
- **Entry:** implementation complete
- **Exit:** quality and security thresholds passed
- **Blockers:** Sev-1/Sev-2 defects, critical vulnerability unresolved
- **Evidence:** test reports, security findings, waivers (if any)
- **Waiver authority:** security-dev for security exceptions (time-bound), qa-dev for non-critical quality exceptions

### Phase 5 — Release Readiness
- **Owner (DRI):** devops-dev + project-manager
- **Entry:** QA/Security gates green
- **Exit:** deployment plan and rollback verified
- **Blockers:** rollback not validated, infra instability
- **Evidence:** release checklist, rollout plan, rollback steps
- **Waiver authority:** devops-dev + orchestrator

### Phase 6 — Post-Release
- **Owner (DRI):** project-manager
- **Entry:** release complete
- **Exit:** incident-free stabilization window or mitigations in place
- **Blockers:** unresolved high-impact incidents
- **Evidence:** post-release report, follow-up backlog
- **Waiver authority:** orchestrator

## Delivery Cadence and SLA Baseline
- Architecture review turnaround: **< 24h** business time
- Blocker escalation response: **< 2h** business time
- Daily async status update cutoff: **17:00 local**
- Weekly milestone review: **1x/week minimum**
- Target lead-time trend: improving week-over-week (DORA-lite)

## Blocking Defect Policy
- No open Sev-1/Sev-2 issues at release gate.
- Any waiver must include: owner, rationale, expiry date, mitigation plan.
