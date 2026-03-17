# Release Gates (Factory Standard)

A change can be considered release-ready only when all gates pass.

## Gate 1 — Product
- Acceptance criteria satisfied
- Scope matches approved story

## Gate 2 — Architecture
- ADR approved for significant changes
- Ownership and interfaces clear

## Gate 3 — Engineering
- Relevant tests executed
- Build/lint/type checks green (if applicable)

## Gate 4 — Security
- No unresolved high/critical risks
- Sensitive data handling verified

## Gate 5 — QA
- Test evidence attached
- Known limitations documented

## Gate 6 — Operations
- Rollback or mitigation plan available
- Monitoring/observability impact reviewed
