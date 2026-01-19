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
│   ├── curriculum/    # Course materials
│   │   └── ai-accelerated-software-development/
│   │       └── foundations/
│   │           ├── 1-fundamentals/  (Weeks 1-2)
│   │           ├── 2-labs/          (Weeks 3-6)
│   │           └── 3-applied/       (Weeks 7-10)
│   ├── client-materials/  # Client-specific deliverables
│   └── marketing/     # Brochures, infographics
├── assets/            # Reusable templates, prompts, images
├── reference/         # Background materials, research, inspiration
└── _project/          # Project meta-docs (session history, etc.)
```

## Course Structure

**Course:** AI Accelerated Software Development
**Level:** Foundations (10-week program)

| Phase | Weeks | Description |
|-------|-------|-------------|
| Fundamentals | 1-2 | Online course work, 20 sessions |
| Labs | 3-6 | Hands-on lab exercises |
| Applied | 7-10 | Guided coaching on learner's actual projects |

> **Product Note:** Fundamentals (Weeks 1-2) is intentionally **tool-agnostic**. It teaches concepts and mental models that apply to ANY AI coding tool. Instructors may demo various tools (Claude Code, Copilot, etc.), but it's not a tutorial on any specific product. Tool-specific skills come in Labs/Applied.

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
| GT Context | `GT.md` | GT (GPT 5.2) instruction file |
| AI Coordination | `COORDINATION.md` | Work log for Claude and GT |
| Product Changelog | `products/CHANGELOG.md` | Track product changes |
| Fundamentals | `products/curriculum/ai-accelerated-software-development/foundations/1-fundamentals/` | Weeks 1-2 |
| Labs | `products/curriculum/ai-accelerated-software-development/foundations/2-labs/` | Weeks 3-6 |
| Applied | `products/curriculum/ai-accelerated-software-development/foundations/3-applied/` | Weeks 7-10 |
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

## AI Assistants

| Name | Model | Role |
|------|-------|------|
| **Claude** (you) | Claude Code CLI | Lead AI — coordinates project, assigns work |
| **GT** | GPT 5.2 | Helper — takes on assigned tasks |

**Either AI can work on anything.** Use `COORDINATION.md` to log work and prevent simultaneous edits.

## Current Focus

Preparing for 10-week Ensemble pilot:
- Weeks 1-2: Fundamentals (20 sessions)
- Weeks 3-6: Labs (hands-on exercises)
- Weeks 7-10: Applied (coaching on real projects)

Primary languages: .NET, Python

## Tooling

**Ensemble Pilot:** Claude (approved) - Claude Code CLI as primary agentic harness

**Future Clients (placeholder):** Some enterprises may be restricted to Windows + GitHub Copilot. Content for Copilot CLI workflows will need to be developed for those engagements.

**Enterprise Constraints:** No external SaaS uploads, PHI/PII redaction required, approved models only
