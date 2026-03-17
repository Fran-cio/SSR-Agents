# Skills Curation for Software Delivery

## Source explored
- https://skills.sh (Agent Skills Directory)
- Microsoft `github-copilot-for-azure`
- `inferen-sh/skills`

## Curation criteria
- Useful for software engineering execution
- Reusable in CI/CD, QA, architecture, or agent tooling
- Avoid purely marketing/content-only skills for this repository scope

## Added external skills (snapshot)

### From Microsoft
- `external/microsoft/markdown-token-optimizer.SKILL.md`
- `external/microsoft/skill-authoring.SKILL.md`
- `external/microsoft/analyze-test-run.SKILL.md`
- `external/microsoft/file-test-bug.SKILL.md`

### From skills.sh ecosystem (`inferen-sh/skills`)
- `external/skills-sh/javascript-sdk.SKILL.md`
- `external/skills-sh/python-sdk.SKILL.md`
- `external/skills-sh/ai-rag-pipeline.SKILL.md`
- `external/skills-sh/web-search.SKILL.md`
- `external/skills-sh/python-executor.SKILL.md`
- `external/skills-sh/agent-browser.SKILL.md`

## Recommended adoption order
1. `markdown-token-optimizer` (keep skill docs lean)
2. `skill-authoring` (standardize new skill creation)
3. `analyze-test-run` + `file-test-bug` (QA automation feedback loop)
4. `python-executor` / `web-search` / `agent-browser` (agent tooling)
5. SDK skills for platform extension work (`javascript-sdk`, `python-sdk`)
