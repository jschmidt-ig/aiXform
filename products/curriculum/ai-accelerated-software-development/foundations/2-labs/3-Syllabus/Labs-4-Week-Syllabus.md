# AI Accelerated Software Development — Labs Syllabus (Weeks 3-6)

This syllabus covers the Labs phase of the Foundations program, optimized for enterprise constraints:
- No external SaaS; no code upload; approved models only
- Coaches operate off-network; participants execute inside their environment
- Azure DevOps friendly; portable later

## Program Context

| Phase | Weeks | Focus |
|-------|-------|-------|
| Fundamentals | 1-2 | Online course work, 20 micro-sessions |
| **Labs** | **3-6** | **Hands-on lab exercises (this syllabus)** |
| Applied | 7-10 | Guided coaching on real projects |

## Time Commitment

- **Total:** 8-10 hours/week
- **Lecture:** ~2 hours (video content + notes)
- **Lab (hands-on):** 5-6 hours (structured lab work)
- **Review:** 1-2 hours (artifact submission + cohort session)

## Week-by-Week Plan

| Week | Lab | Lecture Theme | Lab Focus | Primary Artifacts |
|---:|---|---|---|---|
| 3 | Lab 01 | Enterprise-safe workflow; plan mode; permissions; PR narration | API Foundations: spec → plan → endpoints → tests → PR | API spec + plan output + PR + tests |
| 4 | Lab 02 | Docs-from-code: ADRs, architecture README, risk mapping | Codebase Analysis & Documentation | ADR + architecture README + risk-ranked backlog |
| 5 | Lab 03 | Testing acceleration: unit tests, edge cases, coverage strategy | Testing & Coverage Acceleration | Test plan + coverage delta report |
| 6 | Lab 04 | Observability + Security: logs, correlation IDs, prompt injection defense | Observability, Security & Compliance | Obs module + runbook + security policy |

## Lab Details

### Lab 01: API Foundations (Week 3)
Build a minimal API in a safe sandbox environment. Focus on clean workflow rather than feature richness.

**Deliverables:**
- API contract (OpenAPI YAML or typed interface)
- Plan-mode output with acceptance criteria
- Implementation (minimum 2 endpoints)
- Unit tests (4+ including edge cases)
- PR narration + permissions note

### Lab 02: Codebase Analysis & Documentation (Week 4)
Inspect a production codebase safely (read-only), generate usable documentation, create risk-ranked backlog.

**Deliverables:**
- Architecture README (what it is, how it runs, risks)
- ADR v1 (one major decision with trade-offs)
- Dependency & boundary map notes
- Risk-ranked backlog (top 10 safe PR candidates)

### Lab 03: Testing & Coverage Acceleration (Week 5)
Baseline measurement, high-ROI test selection, coverage delta reporting.

**Deliverables:**
- Coverage baseline (before)
- Test plan (what to test and why)
- New tests (8+ including edge cases)
- Coverage delta report (after)

### Lab 04: Observability, Security & Compliance (Week 6)
Instrument service with observability, run security/compliance drill.

**Deliverables:**
- Structured logging implementation
- Correlation ID propagation
- Runbook (local run + troubleshooting)
- Prompt injection drill findings + mitigations
- Redaction checklist + prompt review workflow

## Approach: Production Codebase Focus

All labs are designed for working with production codebases - real enterprise code that requires careful, methodical approaches:
- Heavier docs + analysis + safe PR selection
- Scaffolding-first approach (tests/docs/observability)
- Risk-aware, incremental improvements

## What Comes Next

After completing Labs (Weeks 3-6), learners move to the **Applied Coaching** phase (Weeks 7-10) where they:
- Apply skills to their actual work projects
- Receive guided coaching support
- Build capstone deliverables
- Prepare executive ROI readout
