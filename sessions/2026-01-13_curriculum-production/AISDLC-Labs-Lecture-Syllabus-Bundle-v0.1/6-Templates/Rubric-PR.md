ChatGPT Folder > AI SDLC Course Productization > Rubric-PR.md
# Rubric — Pull Request (PR) Quality

Score each dimension 0–4.

## Dimensions
1) **Scope & slicing**
- 0: huge PR; unrelated changes
- 2: mostly focused; some noise
- 4: tight scope; logical commits; easy to review

2) **Narration quality**
- 0: no explanation
- 2: basic what/why, missing risk/testing
- 4: what/why/risk/how-tested + follow-ups

3) **Risk management**
- 0: ignores risk
- 2: mentions risk without mitigations
- 4: explicit risks + mitigations + rollback notes

4) **Testing evidence**
- 0: no evidence
- 2: tests exist but unclear
- 4: clear test approach + results + edge cases

5) **Maintainability**
- 0: messy, inconsistent
- 2: acceptable with minor issues
- 4: clean, idiomatic, consistent patterns

## Required evidence
- PR description using the narration template
- Test output (or screenshot/log)
- Link to plan / acceptance criteria (where applicable)
