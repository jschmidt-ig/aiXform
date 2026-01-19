ChatGPT Folder > AI SDLC Course Productization > Lab-04-Observability-Security-Compliance.md
# Lab 04 — Observability + Security/Compliance Drills

## Why this lab exists
Enterprise AI SDLC fails when teams ignore safety and operational reality. This lab teaches:
- minimum viable observability (logs + correlation IDs)
- how to document operational expectations (runbooks)
- prompt redaction and injection defense in real workflows

## Scenario
Instrument the sandbox service (or approved internal service) and then run a security/compliance drill.

## Deliverables
1) Structured logging implemented (with a defined schema)
2) Correlation ID propagation end-to-end
3) Runbook (local run + troubleshooting + log fields)
4) Redaction checklist and “prompt review” workflow
5) Prompt-injection drill findings + mitigations

## Timebox
- 4 hours total

## Steps
### Part A — Observability build (2 hours)
- Add structured logs to request handling.
- Propagate a correlation ID from inbound request through core operations.
- Document log fields (schema) and where to search them.
- Add at least 1 “failure mode” log (e.g., validation failure).

### Part B — Runbook (45–60 min)
- Local setup
- Common failures and fixes
- What good logs look like
- How to verify correlation IDs

### Part C — Security drill (45–60 min)
- Redaction drill: remove sensitive tokens/IDs from prompts
- Prompt injection: attempt to coerce the tool into unsafe behavior; document:
  - the attack prompt
  - what happened
  - mitigations (stop conditions, tool permission limits, output contracts)

## Assessment
- Docs rubric: `6-Templates/Rubric-Docs.md`
- Prompts rubric: `6-Templates/Rubric-Prompts.md`
- PR rubric (if code change submitted): `6-Templates/Rubric-PR.md`
