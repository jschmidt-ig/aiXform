# Lab 02 — Codebase Analysis + Documentation Generation

## Why this lab exists
Enterprise teams work with production codebases. This lab teaches:
- how to inspect a larger repo safely (read-only when needed)
- how to generate usable documentation (not fluff)
- how to create a risk-ranked backlog of safe improvements

## Scenario
You are dropped into a "typical enterprise service" repo (sanitized sample or internal approved repo).
Your job is to produce **clarity**:
- architecture overview
- key boundaries and dependencies
- change-risk heatmap
- top safe PR candidates

## Starting state
- A repository with at least:
  - 2–5 modules/services
  - some tech debt
  - minimal docs

## Constraints
- Prefer read-only in the first pass.
- Do not paste sensitive code into tools outside approved boundaries.
- Docs must be actionable (a new engineer should ramp faster).

## Deliverables
1) **Architecture README** (what it is, how it runs, where risks are)
2) **ADR v1** (one major decision with trade-offs)
3) **Dependency & boundary map notes**
4) **Risk-ranked backlog** (top 10 safe PR candidates)
5) **"Safe PR" pick**: choose 1 and outline plan + acceptance criteria

## Timebox
- 4 hours total

## Steps
### Step 1 — Repo inventory (30–45 min)
- Identify entry points, build/run steps, deployment path (if known).
- Identify high-level modules and ownership boundaries.

### Step 2 — Dependency & boundary mapping (45–60 min)
- Map dependencies between modules.
- Identify data boundaries and "sensitive zones".
- Identify hot spots: high churn + low tests + complex code.

### Step 3 — Generate the docs pack (60–90 min)
- Write an Architecture README (use the template in `6-Templates/` or your own).
- Draft an ADR for one decision (e.g., logging standard, module boundary, error handling pattern).

### Step 4 — Produce a safe backlog (45–60 min)
Create a top 10 backlog of PR candidates that are:
- low risk
- high leverage
- minimal coupling
Examples:
- add missing tests to a stable module
- add structured logging wrapper
- create runbook
- add CI gates
- add doc generation scripts

### Step 5 — Pick one safe PR and plan it (20–30 min)
- define acceptance criteria
- define rollback strategy
- define "how tested"

## Assessment
- Docs rubric: `6-Templates/Rubric-Docs.md`
- PR rubric: `6-Templates/Rubric-PR.md` (for the plan + narration quality)
