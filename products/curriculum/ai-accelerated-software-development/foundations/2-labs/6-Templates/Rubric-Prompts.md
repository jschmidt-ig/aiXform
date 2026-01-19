ChatGPT Folder > AI SDLC Course Productization > Rubric-Prompts.md
# Rubric — Prompts (Plan mode / Code gen / Docs gen)

Score each dimension 0–4.

## Dimensions
1) **Context & constraints**
- 0: missing context
- 2: partial constraints
- 4: clear constraints, enterprise-safe boundaries

2) **Output contract**
- 0: no structure
- 2: some structure
- 4: explicit sections, formats, acceptance criteria

3) **Redaction & safety**
- 0: leaks secrets/sensitive data
- 2: basic redaction
- 4: explicit redaction rules + safe examples

4) **Determinism**
- 0: vague
- 2: moderately specific
- 4: specific; minimizes hallucination; includes checks

5) **Review & stop conditions**
- 0: none
- 2: minimal
- 4: explicit human review steps and stop conditions

## Required evidence
- Prompt text (or link)
- Output sample (sanitized)
- Notes on what was redacted and why
