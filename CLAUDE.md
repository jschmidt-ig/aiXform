# aiXform Project Context

## What This Is

aiXform is an AI transformation training company targeting enterprise software development. This repository contains business planning, strategy, curriculum development, and client materials.

**Parent Company:** Integral Dragon (consulting)
**First Client:** Ensemble Health Partners (10-week pilot starting mid-January 2026)

## Directory Structure

```
aiXform/
├── sessions/          # Time-boxed working sessions (YYYY-MM-DD_description)
├── products/          # Finished, extracted deliverables
│   ├── curriculum/    # Course materials (labs, fundamentals)
│   ├── client-materials/  # Client-specific deliverables
│   └── marketing/     # Brochures, infographics
├── assets/            # Reusable templates, prompts, images
├── reference/         # Background materials, research, inspiration
└── _project/          # Project meta-docs (session history, etc.)
```

## Session Convention

Sessions are named: `YYYY-MM-DD_short-description`

**Multiple sessions on the same day:** Use a numeric suffix when doing different logical tasks on the same day:
- `2026-01-19-1_project-organization`
- `2026-01-19-2_gap-analysis`

Each session should contain:
- `SESSION.md` - Summary of goals, outcomes, decisions, and what was extracted
- `_input/` - Materials that came into the session
- `_scratch/` - Working files, experiments, iterations
- `_output/` - Session deliverables (candidates for extraction to products/)

## Key Documents

| Document | Location | Purpose |
|----------|----------|---------|
| Project Overview | `README.md` | Business context and background |
| Current Status | `PROJECT-STATUS.md` | Session-by-session progress |
| Labs Bundle | `products/curriculum/labs-bundle/` | 8-week hands-on labs (Weeks 3-10) |
| Fundamentals Bundle | `products/curriculum/fundamentals-bundle/` | 2-week foundation course (Weeks 1-2) |
| Client Pitch | `products/client-materials/ensemble/` | Ensemble-specific materials |

## Business Model

| Tier | Name | Price | Format |
|------|------|-------|--------|
| L1 | Foundations | $300-500/seat | Self-paced, recorded |
| L2 | Practitioner | $2,000-3,000 | 10-week cohort with labs |
| L3 | Enterprise Accelerator | $30,000-50,000 | Team coaching |

## AI SDLC Maturity Model

| Level | Name | Human Role |
|-------|------|------------|
| 1 | Autocomplete Assist | Author |
| 2 | Supervised Agent Coding | Pair programmer |
| 3 | PR-Submitting Agent | Reviewer |
| 4 | Multi-Agent Orchestration | Tech Lead |
| 5 | Agent Org/Hierarchical Team | Manager |

## Team

- **Dragon** - Founder, executive relationships
- **Justin** - AI development expert, curriculum
- **Danny** - Training & instructional design
- **Scot** - Chief of staff, client management

## Current Focus

Preparing for 10-week Ensemble pilot:
- Weeks 1-2: Fundamentals (20 micro-sessions)
- Weeks 3-10: Labs & Applied (5 hands-on labs)

Primary languages: .NET, Python
Enterprise constraints: Windows + GitHub Copilot, no external SaaS, PHI/PII redaction required
