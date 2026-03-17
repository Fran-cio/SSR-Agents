# Quality and Security Gate Policy

## Quality Gates (qa-dev owner)
- CI tests must pass: **100% required suites green**
- Critical-path smoke tests: **required before merge/release**
- Release blocker defects: **no open Sev-1/Sev-2**
- Flaky tests: quarantine and owner assignment within 24h

## Security Gates (security-dev owner)
- Secrets scanning required pre-merge
- Dependency scanning required pre-merge
- Container/IaC scan required for infra-affecting changes
- Threat model required for medium/high-risk changes
- AuthN/AuthZ checklist required on identity-sensitive changes

## Exception Process
Any gate exception must include:
- Exception owner
- Scope affected
- Risk rationale
- Mitigation actions
- Expiration date
- Explicit approver
