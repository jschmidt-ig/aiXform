# Session Handoff - Resume Point

**Last Session:** January 19, 2026

## What We Did This Session

1. **Reorganized the entire project structure** for maintainability by Claude
2. Renamed `log/` to `sessions/` with date-based naming (`YYYY-MM-DD_description`)
3. Created `products/` directory for extracted finished work
4. Created `assets/` and `reference/` directories
5. Created `CLAUDE.md` root context file
6. Added `SESSION.md` files to each session for documentation

## New Directory Structure

```
aiXform/
├── CLAUDE.md              # Claude context file
├── README.md              # Project overview
├── PROJECT-STATUS.md      # Current state
├── sessions/              # Time-boxed working sessions
│   ├── 2026-01-07_market-research/
│   ├── 2026-01-08_research-consolidation/
│   ├── 2026-01-10_client-alignment/
│   ├── 2026-01-11_maturity-model/
│   ├── 2026-01-12_operational-planning/
│   ├── 2026-01-13_curriculum-production/
│   ├── 2026-01-14_visual-assets/
│   ├── 2026-01-15_final-infographics/
│   └── 2026-01-16_research-classes/
├── products/              # Extracted finished work
│   ├── curriculum/
│   │   ├── labs-bundle/
│   │   └── fundamentals-bundle/
│   ├── client-materials/ensemble/
│   └── marketing/
│       ├── brochures/
│       └── infographics/
├── assets/                # Reusable templates, prompts
└── reference/             # Background materials
    ├── inspiration/
    ├── integral-dragon-strategy/
    └── market-research/
```

## Session Conventions

**Naming:** `YYYY-MM-DD_short-description`
- Multiple sessions same day: `2026-01-19-1_task-one`, `2026-01-19-2_task-two`

Each session folder should contain:
- `SESSION.md` - Summary: goal, outcomes, decisions, what was extracted
- `_input/` - Materials that came into the session
- `_scratch/` - Working files, experiments
- `_output/` - Deliverables (candidates for extraction)

## Key Files

| File | Purpose |
|------|---------|
| `CLAUDE.md` | Context for Claude to understand the project |
| `PROJECT-STATUS.md` | Detailed status with all sessions |
| `products/curriculum/labs-bundle/` | 8-week labs course materials |
| `products/curriculum/fundamentals-bundle/` | 2-week fundamentals course |
| `products/marketing/brochures/` | HTML brochures |

## Where We Left Off

Project structure is now organized. Next priorities from previous session:

1. **Gap analysis** - what exists (specs) vs what needs to be created (actual content)
2. **Content production schedule** - what to build first for the mid-January start
3. **Environment setup** - sandbox repos, lab infrastructure

## To Resume

Tell Claude: "Read CLAUDE.md and let's continue with [your task]"

## Quick Context

- **aiXform** = new AI transformation training company
- **Integral Dragon** = parent consulting company
- **Ensemble Health Partners** = first client, 10-week pilot starting mid-January
- **Team:** Dragon (founder), Justin (you - AI dev expert), Danny (training), Scot (ops)
