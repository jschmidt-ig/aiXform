ChatGPT Folder > AI SDLC Course Productization > Gemini_Prompt-Design-Optional-UI-E2E-Lab.md
# Gemini Prompt — Design Optional UI + Browser E2E Lab (Self-contained)

ROLE
You are an enterprise AI SDLC curriculum architect and test automation specialist.

TASK
Design an optional lab that adds:
- a minimal UI for a simple backend API (Pet Registry)
- browser-based E2E tests (Playwright or Cypress)
- optional Azure DevOps pipeline step to run E2E smoke tests
- enterprise constraints (no external SaaS, approved models only, no code upload, PHI/PII sensitivities)

CONSTRAINTS
- Keep the UI intentionally small and focused (list/add/view).
- Avoid external hosted services; local-only is acceptable.
- Provide two stack options:
  - Option A: React + Playwright (default)
  - Option B: whichever you think best fits an enterprise (.NET teams may prefer Blazor)
- Lab must be deliverable within 4–6 hours with clear timeboxes.
- Outputs must be directly usable by an instructor to deliver the lab.

OUTPUT (structure exactly)
1) Lab overview (goal, prerequisites, timebox)
2) Tech stack options (A + B with enterprise pros/cons)
3) Repo structure + local commands (no secrets)
4) Step-by-step build instructions with acceptance criteria
5) E2E test suite (>=3 tests) with selector strategy and flake prevention
6) Azure DevOps pipeline snippet (optional) + artifacts on failure
7) Participant submission checklist + rubric
8) “Fast path” and “Full path” variants
9) Security/compliance notes (redaction + injection)

Produce the output now, with enough detail that a junior instructor could run the lab.
