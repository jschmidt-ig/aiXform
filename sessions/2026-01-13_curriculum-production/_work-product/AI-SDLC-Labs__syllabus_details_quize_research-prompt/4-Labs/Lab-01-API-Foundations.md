ChatGPT Folder > AI SDLC Course Productization > Lab-01-API-Foundations.md
# Lab 01 — API Foundations (Safe Sandbox)

## Why this lab exists
Week 1 must work even when enterprise approvals are slow. This lab creates a **safe, non-sensitive** project that teaches:
- plan mode / task decomposition
- permissions boundaries (what the tool can/can’t do)
- diff-first development + human review
- PR narration (what/why/risk/how-tested)

## Scenario
Build a minimal “Pet Registry” API for an enterprise team. Keep it intentionally small:
- CRUD-lite for pets (Create, Get, List)
- Optional: owner association (read-only)

This is not about feature richness; it’s about clean workflow.

## Starting state
- A “sandbox repo” provided by the course (or created internally), containing:
  - `README.md` with constraints
  - project skeleton in one language: **.NET / Java / Python**
  - basic test harness (empty tests folder is fine)

## Constraints (non-negotiable)
- No sensitive business logic or data.
- No external SaaS dependencies.
- Everything must be runnable locally.
- AI outputs must be reviewed before commit.

## Deliverables (what participants submit)
1) **API contract** (OpenAPI YAML/JSON OR a typed interface + doc)
2) **Plan-mode output** (task decomposition + acceptance criteria)
3) **Implementation** (at least 2 endpoints)
4) **Unit tests** (minimum 4 tests, with at least 2 edge cases)
5) **PR narration** (what/why/risk/how-tested)
6) **Permissions + data-handling note** (1 page max)

## Timebox
- Lab block #1: 2 hours
- Lab block #2: 2 hours
- Optional stretch: 30–60 minutes

## Steps
### Step 1 — Define the API (20–30 min)
- Write endpoints and inputs/outputs.
- Define validation rules (e.g., name required; species enum; age non-negative).
- Define error taxonomy (400 vs 404 vs 500) at a high level.

### Step 2 — Plan mode decomposition (15–25 min)
Use plan mode to produce:
- atomic tasks (5–12)
- acceptance criteria per task
- risk notes (what could go wrong)
- “stop conditions” (when to ask for human review)

### Step 3 — Implement iteratively with diff-first review (60–90 min)
- Implement 1 endpoint end-to-end.
- Review diff for:
  - correctness
  - security footguns
  - needless complexity
- Commit in small slices.

### Step 4 — Add tests (30–60 min)
Minimum set:
- happy path for Create
- validation failure for Create
- Get by id success
- Get by id not-found

Edge cases examples:
- invalid enum
- oversized payload
- duplicate IDs (if applicable)

### Step 5 — PR narration + risk note (15–20 min)
Use the PR narration template:
- What changed
- Why
- Risk
- How tested
- Follow-ups

## Stretch goals (optional)
- Add API docs generation step (markdown from OpenAPI)
- Add minimal CI check (run tests on PR)
- Add simple structured logging for requests

## Assessment
Use these rubrics:
- `6-Templates/Rubric-PR.md`
- `6-Templates/Rubric-Tests.md`
- `6-Templates/Rubric-Prompts.md`
- `6-Templates/Rubric-Docs.md` (if docs included)
