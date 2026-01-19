ChatGPT Folder > AI SDLC Course Productization > ADO-Pipeline-Gates-Checklist.md
# Azure DevOps (ADO) Pipeline Gates Checklist

Use this as a planning checklist; adapt to your org templates.

## Minimum gates (recommended)
- Build succeeds
- Unit tests run
- Coverage report generated (even if threshold is 0 initially)
- Lint/static analysis (optional)
- Artifact publishing on failure (logs; screenshots for E2E if used)

## Practices
- Start with “report only” before enforcing thresholds
- Add thresholds gradually (avoid breaking teams)
- Ensure failure messages tell engineers how to fix the issue
- Keep pipeline time reasonable (fast feedback)

## Evidence to collect in labs
- Pipeline YAML snippet or screenshot
- Example failure + fix walkthrough
