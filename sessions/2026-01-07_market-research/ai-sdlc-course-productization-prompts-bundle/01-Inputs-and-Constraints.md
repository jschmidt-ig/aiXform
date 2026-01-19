ChatGPT Folder > AI SDLC Product Strategy > 01-Inputs-and-Constraints.md

# Captured answers (Justin)

## A) Audience + outcomes
- Outcomes: open to suggestions; wants metrics that are controllable; suggested:
  - Delivery velocity (cycle time: idea → coded → tested → production)
  - Quality / experience survey (NPS-like or perceived value of course delivery)

- Day 1 differences:
  - Assume repo access + permissions.
  - Tool constraints: may not be able to install Claude Code CLI on workstations; may need an internal Claude model setup.
  - Assume by end of week 1 they will have access to needed tools.
  - Need content/workarounds for week 1 while setup happens.

- Skill baseline:
  - Ensemble: mid/senior SWEs; varying Copilot experience; competent in Git; decent testing maturity.
  - Cigna infra/data engineers: less experienced; basic scripting; likely little/no LLM or Git tooling exposure (maybe consumer ChatGPT/Copilot).

## B) Delivery logistics (10-week reality)
- First 10 weeks: synchronous, live lecture/demo + hands-on lab.
- Later: transition to asynchronous/self-paced, with optional office hours.
- Cohort targets:
  - Tier 1 (training-heavy): 100–200 (possibly enterprise-wide)
  - Tier 2 (hybrid): 20–25
  - Tier 3 (coaching-heavy): 3–5
- Duration/cadence: 10 weeks is initially driven by contract; open to alternative productized formats:
  - 1–2 hours/day model
  - “bootcamp” model (e.g., ~6 hours/day)
  - Wants AI to propose common models and best fit.

## C) Tooling + constraints
- “quad code” is a typo → **Claude Code CLI** is the primary coding assistant.
- Constraints: assume strict enterprise controls:
  - no external SaaS / no code upload
  - approved models only
  - security/red-team reviews
  - PHI/PII sensitivities
- Coach access constraint:
  - Prefer not needing provisioned corporate laptops or internal access; want to assist “off network.”

- Stack preferences:
  - Both clients: Azure; repos in ADO (Azure DevOps).
  - Product should later generalize to AWS and be language-independent.
  - Likely need parallel examples: .NET, Java, Python.
  - Ensemble examples: .NET
  - Internal demos: Python

## D) Product model + pricing
- Placeholder pricing was exploratory; wants market-driven options.
- Pricing unit: one-time training + X weeks support (not annual), flexible.
- Open to team packs.
- Gross margin not defined; wants recommended targets.

## E) Positioning + naming
- Not in love with “belt” terminology; open to alternatives; wants more professional.
- Tone: professional with personality; not overly corporate; enterprise buyers.
- Certification/badge: open (not explicitly requested, but implied as option).
