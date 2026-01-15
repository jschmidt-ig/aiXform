ChatGPT Folder > AI SDLC Course Productization > Rubric-Tests.md
# Rubric — Tests

Score each dimension 0–4.

## Dimensions
1) **Coverage focus**
- 0: tests unrelated to risk
- 2: some coverage, low ROI
- 4: targets high-risk/high-churn areas

2) **Edge cases**
- 0: only happy paths
- 2: a few edge cases
- 4: thoughtful edge cases + negative paths

3) **Determinism**
- 0: flaky/non-deterministic
- 2: mostly stable
- 4: deterministic; no time/network dependencies

4) **Readability**
- 0: unreadable
- 2: ok
- 4: clear naming, structure, intent

5) **Maintainability**
- 0: brittle snapshots/mocks
- 2: some brittleness
- 4: stable selectors/mocks; minimal coupling

## Required evidence
- Baseline + post-lab coverage numbers (if coverage measured)
- Short test plan describing what/why
