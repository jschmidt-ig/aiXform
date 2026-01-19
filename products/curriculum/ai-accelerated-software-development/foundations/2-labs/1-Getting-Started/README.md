ChatGPT Folder > AI SDLC Course Productization > README.md
# AISDLC Bundle v0.1: Labs + Lecture Series + Syllabus + Marketing

## What this bundle is
This bundle contains:
- A **4-lab core sequence** for enterprise AI SDLC enablement (plus **1 optional UI/E2E lab**)
- A **10-week syllabus** (lecture + lab + applied blocks)
- A **23-minute “lecture series” episode syllabus** aligned to enterprise delivery constraints
- A simple **marketing HTML landing page** for the labs
- **Rubrics + templates** for repeatable delivery
- **Self-contained prompts** you can paste *as-is* into ChatGPT Pro (Research) or Gemini to generate/extend materials

Everything is designed for:
- Enterprise constraints (no external SaaS, no code upload, approved models only, PHI/PII sensitivities)
- Off-network coaching (participants run tools inside their environment)
- Azure DevOps repo reality (but portable to GitHub later)

## Directory map
- `1-Getting-Started/`
  - `README.md` (this file)
  - `Quickstart.md` (how to deliver Week 1)
- `2-Marketing/`
  - `Labs-Landing-Page.html`
- `3-Syllabus/`
  - `10-Week-Syllabus.md` (lecture/lab/applied blocks)
  - `Lecture-Series-23min-Episodes.md` (episode-by-episode)
  - `Student-Schedule-Practitioner.md` (8-10h/week cadence)
- `4-Labs/`
  - `Lab-01-API-Foundations.md`
  - `Lab-02-Codebase-Analysis-DocGen.md`
  - `Lab-03-Testing-Coverage-Acceleration.md`
  - `Lab-04-Observability-Security-Compliance.md`
  - `Lab-05-Optional-UI-E2E-Automation.md`
- `5-Prompts/`
  - `ChatGPT-Pro-Research_Prompt-Design-Optional-UI-E2E-Lab.md`
  - `Gemini_Prompt-Design-Optional-UI-E2E-Lab.md`
- `6-Templates/`
  - `Rubric-PR.md`, `Rubric-Tests.md`, `Rubric-Docs.md`, `Rubric-Prompts.md`
  - `Codebase-Analysis-Worksheet.md`
  - `Lesson-Plan-Template.md`
  - `Lab-Template.md`
  - `Prompt-Pattern-Library-Template.md`
  - `ADO-Pipeline-Gates-Checklist.md`

## How to use this bundle
### If you’re delivering live (recommended for MVP)
1) Use `3-Syllabus/10-Week-Syllabus.md` as the master plan.
2) Each week:
   - Deliver the week’s lecture(s) (use `3-Syllabus/Lecture-Series-23min-Episodes.md` as your script outline)
   - Run the lab(s) from `4-Labs/`
   - Collect the required artifacts and score using `6-Templates/*Rubric*`
3) Publish “best artifacts” (sanitized) back into your course repo as exemplars.

### If you’re productizing asynchronously
1) Record each lecture episode (23 minutes).
2) Convert each lab into a “lab pack”:
   - starter repo state (tag/branch), instructions, rubric, solution key
3) Use the prompts in `5-Prompts/` to accelerate authoring and variants.

## Minimum tooling assumptions
- Git + language runtime (.NET OR Java OR Python)
- A “safe sandbox” repo (no sensitive code)
- Approved LLM access (in-product or gateway); if CLI/agent tools aren’t approved in Week 1, use the fallback steps in Week 1.

## Outcomes you can measure (recommendation)
Controllable metrics (good for course ROI):
- PR throughput (PRs merged per dev per week)
- Test coverage delta on targeted module(s)
- Docs completeness (rubric-scored ADR/readme/runbook)
- Time-to-first-safe-PR in sandbox

Lagging / org-dependent metrics:
- Lead time to production, deployment frequency, change failure rate (track, but don’t promise)

## Version
- Bundle: v0.1
- Generated: January 13, 2026
