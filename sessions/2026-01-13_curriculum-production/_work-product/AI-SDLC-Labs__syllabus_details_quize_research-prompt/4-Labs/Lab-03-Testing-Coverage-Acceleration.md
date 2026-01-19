ChatGPT Folder > AI SDLC Course Productization > Lab-03-Testing-Coverage-Acceleration.md
# Lab 03 — Testing + Coverage Acceleration

## Why this lab exists
AI is most valuable when it improves confidence. This lab teaches:
- baseline measurement
- high-ROI test selection
- coverage delta reporting
- keeping AI-generated tests maintainable

## Scenario
Pick a module with weak coverage (sandbox or approved repo). Improve coverage and quality without introducing flakiness.

## Constraints
- Tests must be readable and deterministic.
- Prefer unit tests unless integration tests are necessary.
- Do not generate massive snapshots that become unmaintainable.

## Deliverables
1) Coverage baseline (before)
2) Test plan (what you will test and why)
3) New tests (minimum 8 total, including edge cases)
4) Coverage delta report (after)
5) Notes on any refactoring required to enable testing

## Timebox
- 4 hours total

## Steps
1) **Baseline coverage (20–30 min)**  
   Record current coverage for the target module.
2) **Select test targets (20–30 min)**  
   Pick 2–3 functions/components that are high risk or high churn.
3) **Generate tests with a human review loop (90–120 min)**  
   - generate test cases
   - rewrite for clarity
   - add edge cases
4) **Stabilize and rerun coverage (30–45 min)**  
   Ensure tests pass consistently.
5) **Write the coverage delta report (15–20 min)**  
   Show before/after and explain what changed.

## Assessment
- Tests rubric: `6-Templates/Rubric-Tests.md`
- PR rubric (if submitted as PR): `6-Templates/Rubric-PR.md`
