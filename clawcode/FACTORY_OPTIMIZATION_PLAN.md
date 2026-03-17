# Factory Optimization Plan (v1)

## Objective
Make the SR2 agent team faster, more reliable, and easier to operate for software delivery.

## Priority Changes

### P0 — Delivery Control Plane
1. **Architecture gate required** before any large implementation.
2. **Definition of Ready (DoR)** for each story:
   - business goal
   - acceptance criteria
   - dependencies
   - owner
3. **Definition of Done (DoD)** evidence bundle:
   - changed artifacts
   - tests run + results
   - security/QA check status

### P0 — Handoff Standardization
Every delegation must include:
- Context and objective
- Scope limits
- Acceptance criteria
- Risks/dependencies
- Expected output format

Every completion report must include:
- What changed
- Validation evidence
- Open risks
- Next action

### P1 — Shift-left Quality/Security
- QA and Security review start at design stage, not post-implementation.
- Mandatory pre-merge checklist for backend/frontend/fullstack/smart-contract work.

### P1 — Operational Cadence
- Daily triage: blockers + dependencies + risk review.
- Milestone updates to stakeholders on each meaningful advance.

## Role-Level Improvements
- **orchestrator**: delegation-first, no heavy implementation unless explicitly requested.
- **lead-architect**: ADR template required for non-trivial system changes.
- **project-manager**: dependency map maintained per sprint.
- **qa-dev + security-dev**: explicit gate status in each release candidate.

## KPIs
- Lead time from assignment to first review
- Reopen rate due to unclear requirements
- Defect escape rate
- Blocker aging time
- % tasks with complete handoff packet
