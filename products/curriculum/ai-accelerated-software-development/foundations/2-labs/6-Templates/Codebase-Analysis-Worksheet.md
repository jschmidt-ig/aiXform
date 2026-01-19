# Production Codebase Analysis Worksheet (Read-only friendly)

## Repo context
- Repo name:
- Language(s):
- Build system:
- Deployment model:
- Primary owners:

## Quick inventory
- Entry points:
- Top modules/services:
- External dependencies:
- Data stores:
- “Sensitive zones” (PHI/PII, credentials, regulated data):

## Dependency + boundary map (notes)
- Module A depends on:
- Module B depends on:
- Cross-cutting concerns:
- Boundary violations / tight coupling:

## Risk heatmap (notes)
List hot spots with reasons:
- Hot spot 1:
- Hot spot 2:
- Hot spot 3:

## Testing baseline
- Current coverage (if known):
- Most critical untested areas:

## Observability baseline
- Logging present? (Y/N)
- Correlation IDs? (Y/N)
- Tracing? (Y/N)
- Metrics? (Y/N)

## Top 10 “safe PR” candidates
Ranked list, each with:
- Candidate:
- Why low-risk:
- Expected impact:
- How to test:
- Rollback plan:

## Suggested 4-week PR sequence
Week 1:
Week 2:
Week 3:
Week 4:

## Notes on constraints
- Tooling approvals:
- What cannot be shared outside environment:
- Redaction rules used:
