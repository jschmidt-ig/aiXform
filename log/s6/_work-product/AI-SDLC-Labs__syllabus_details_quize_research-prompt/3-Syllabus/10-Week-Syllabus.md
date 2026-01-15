ChatGPT Folder > AI SDLC Course Productization > 10-Week-Syllabus.md
# AI SDLC Enablement — 10-Week Syllabus (Lecture + Lab + Applied)

This syllabus is optimized for enterprise constraints:
- No external SaaS; no code upload; approved models only
- Coaches operate off-network; participants execute inside their environment
- Azure DevOps friendly; portable later

## Structure per week
- **Lecture (asynchronous):** ~1 hour total (2–3 episodes, 23 minutes each, plus notes)
- **Lab (hands-on):** 4 hours total (2 blocks)
- **Applied (in-repo):** 1 hour (artifact submission + reflection); for Accelerator tier, applied expands

## Week-by-week plan (Practitioner baseline)

| Week | Lecture theme (1h) | Lab focus (4h) | Applied / submission (1h) | Primary artifacts |
|---:|---|---|---|---|
| 1 | Enterprise-safe workflow kickoff; plan mode; permissions; PR narration | **Lab 1: API Foundations** (spec → plan → endpoints → tests → PR) | Submit PR + plan + prompt notes | API spec + plan output + PR + tests |
| 2 | CLI-driven delivery loop: ticket → plan → diff → review | Extend API with a new feature + refactor for clarity | PR narration + risk notes | PR + risk/QA notes |
| 3 | Testing acceleration: unit tests, edge cases, coverage strategy | **Lab 3: Testing + Coverage** on the sandbox repo | Coverage delta report | Test plan + coverage delta |
| 4 | Docs-from-code: ADRs, architecture README, diagrams | **Lab 2: Brownfield inspection + doc generation** (sanitized repo) | Submit ADR + architecture pack | ADR + architecture README |
| 5 | Brownfield analysis mechanics: dependency map, boundaries, risk | Brownfield worksheet run (read-only on real repo) | Ranked backlog of safe PRs | Worksheet + ranked backlog |
| 6 | “Safe PR” strategy: scaffolding-only, non-invasive improvements | Implement a scaffold PR (tests/docs/obs sidecar) | Rollout plan + review notes | Safe PR + rollout plan |
| 7 | CI/CD quality gates: lint/test/coverage thresholds | Add gates to pipeline templates (ADO oriented) | Runbook “how to fix failures” | Pipeline template + runbook |
| 8 | Observability patterns: logs/metrics/traces; correlation IDs | **Lab 4: Observability module** + runbook | Instrumentation checklist | Obs module + runbook |
| 9 | Security & compliance: redaction, prompt injection, tool permissions | **Lab 4 drill component:** red-team prompt drill + policy | Prompt policy + checklist | Policy + drill findings |
| 10 | Capstone + ROI readout: before/after, executive narrative | Capstone PRs + KPI deltas | Exec readout draft | Capstone PR(s) + KPI report |

## Tracks (delta-only)
### Greenfield track (if the team is building new modules)
- Weeks 2–4: focus on building new endpoints/services in the sandbox, plus tests and docs
- Weeks 6–8: focus on CI/CD gates + observability in the new module

### Brownfield track (recommended default in enterprise)
- Weeks 4–6: heavier docs + analysis + safe PR selection
- Weeks 6–10: “scaffolding-first” PRs (tests/docs/observability) before core logic changes

## Week 1 “tooling not ready” fallback
If CLI/agent tooling approvals slip:
- Keep Week 1 in the sandbox repo using chat UI prompts + manual workflows
- Delay “agent CLI mechanics” to Week 2–3
- Still produce: spec, plan, tests, PR narration, and compliance notes
