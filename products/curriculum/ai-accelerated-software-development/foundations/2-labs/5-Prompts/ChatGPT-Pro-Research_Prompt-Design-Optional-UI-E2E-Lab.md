ChatGPT Folder > AI SDLC Course Productization > ChatGPT-Pro-Research_Prompt-Design-Optional-UI-E2E-Lab.md
# ChatGPT Pro (Research) Prompt — Design Optional UI + Browser E2E Lab (Self-contained)

You are an enterprise AI SDLC curriculum architect. Your job: design a production-grade **optional lab** that adds:
- a minimal UI for a simple backend API (Pet Registry)
- browser-based E2E tests (Playwright or Cypress)
- optional CI integration (Azure DevOps friendly)
- enterprise constraints (no external SaaS, approved models only, no code upload, PHI/PII sensitivities)

## Non-negotiable constraints
- Assume strict enterprise controls:
  - no external SaaS, no code upload
  - only approved models/tools inside the client environment
  - coaches operate off-network (participants execute)
- Keep the UI intentionally small and focused.
- Favor stacks that are common in enterprise.
- Must be deliverable as a 4–6 hour lab with clear timeboxes.

## Output requirements (structure exactly)
1) **Lab overview**
   - goal, audience, prerequisites, timebox
2) **Tech stack options**
   - Option A (default) + Option B (alternative)
   - Pros/cons for enterprise constraints
3) **Repo plan**
   - folder structure
   - local dev commands
   - environment config (no secrets)
4) **Step-by-step lab instructions**
   - steps with time estimates
   - acceptance criteria per step
   - “stop conditions” when human review is required
5) **E2E testing plan**
   - at least 3 tests (happy path + negative path)
   - selector strategy (stability)
   - flake avoidance practices
6) **CI integration (ADO-friendly)**
   - YAML snippet for running tests (if feasible)
   - artifact capture on failure (screenshots/videos)
7) **Artifacts and submission**
   - what participants submit
   - scoring rubric mapping
8) **Rubrics (include)**
   - E2E rubric
   - UI code rubric
   - PR narration rubric section specific to UI changes
9) **Security + compliance section**
   - redaction guidance (what not to include)
   - prompt injection risk in UI automation contexts
10) **Variants**
   - “fast path” (2–3 hours) and “full path” (6 hours)

## Context you must assume (do not ask follow-up questions)
- Backend API exists from Lab 1 (Pet Registry).
- Target audience: enterprise engineers (software + infra/data).
- Repo hosting: Azure DevOps or equivalent.
- Goal: teach repeatable SDLC technique, not to build a fancy product.

Now produce the output.
