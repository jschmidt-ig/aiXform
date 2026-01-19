# Session Handoff - Resume Point

**Last Session:** January 19, 2026
**Sessions Today:** 2026-01-19_project-reorganization, 2026-01-19-2_product-restructure

---

## How to Start a New Claude Session

**Tell Claude:**
> Read CLAUDE.md, PROJECT-STATUS.md, and this file (next-step.md). Then let's continue with [your task].

---

## What This Project Is

**aiXform** is a new AI transformation training company being spun out from Integral Dragon (consulting). We're building enterprise AI-assisted development courses.

**First Client:** Ensemble Health Partners - 10-week pilot starting mid-January 2026

**Team:**
- Dragon (Founder) - Executive relationships
- Justin (you) - AI development expert, curriculum
- Danny - Training & instructional design
- Scot - Client management

---

## Current Course: AI Accelerated Software Development - Foundations

A 10-week program with three phases:

| Phase | Weeks | Focus | Time/Week |
|-------|-------|-------|-----------|
| Fundamentals | 1-2 | Online course work, 20 sessions | 4 hrs |
| Labs | 3-6 | Hands-on lab exercises (4 labs) | 8-10 hrs |
| Applied | 7-10 | Guided coaching on real projects | 8-10 hrs |

**Location:** `products/curriculum/ai-accelerated-software-development/foundations/`

---

## Directory Structure

```
aiXform/
├── CLAUDE.md              # Read this first - project context for Claude
├── README.md              # Business overview
├── PROJECT-STATUS.md      # Current state, key documents, gaps
├── next-step.md           # This file - session handoff
│
├── sessions/              # Time-boxed working sessions (YYYY-MM-DD_description)
│   └── [each has SESSION.md documenting work done]
│
├── products/              # Finished deliverables
│   ├── CHANGELOG.md       # Track all product changes
│   ├── curriculum/ai-accelerated-software-development/foundations/
│   │   ├── 1-fundamentals/
│   │   ├── 2-labs/
│   │   └── 3-applied/
│   ├── client-materials/ensemble/
│   └── marketing/brochures/, infographics/
│
├── assets/                # Reusable templates, prompts
├── reference/             # Background materials, research
└── _project/              # Project meta-docs (session-history.md)
```

---

## Session Conventions

**Naming:** `YYYY-MM-DD_short-description`
- Multiple sessions same day: `2026-01-19-1_task-one`, `2026-01-19-2_task-two`

**Each session folder contains:**
- `SESSION.md` - Goals, outcomes, decisions, what was extracted
- `_input/` - Materials that came into the session
- `_scratch/` - Working files, experiments
- `_output/` - Deliverables (candidates for extraction to products/)

**Workflow:**
1. Start session: Create `sessions/YYYY-MM-DD_description/`
2. Work in session using standard subdirs
3. Document outcomes in `SESSION.md`
4. Extract finished work to `products/`
5. Update `products/CHANGELOG.md` with changes

---

## Key Terminology Decisions

| Don't Say | Say Instead |
|-----------|-------------|
| AI SDLC | AI Accelerated Software Development |
| Brownfield | Production Codebase |
| Greenfield/Brownfield tracks | (Eliminated - everyone does same path) |

---

## What Exists (Complete)

- Business model and pricing (L1/L2/L3 tiers)
- 10-week delivery framework
- Course structure (Fundamentals → Labs → Applied)
- Fundamentals syllabus (20 sessions)
- Labs syllabus (4 labs over 4 weeks)
- Lab specifications (Lab 01-04)
- Maturity model framework
- Client pitch documents
- Templates for lessons, labs, assessments
- Marketing brochures

---

## What Needs Creation (Gaps)

### Immediate Priority
- **Applied Coaching phase content** (Weeks 7-10) - currently just a README placeholder
- Slide decks for 20 Fundamentals sessions
- Recorded video content for Weeks 1-2

### Also Needed
- Detailed lab instructions with step-by-step guidance
- Starter code and production codebase examples
- Safe sandbox environments
- Assessment answer keys
- Instructor facilitation guides

---

## Tooling

**Ensemble Pilot:** Claude (approved) - Claude Code CLI as primary agentic harness

**Future Clients (placeholder):** Some enterprises may be restricted to Windows + GitHub Copilot. Content for Copilot CLI workflows will need to be developed for those engagements.

## Enterprise Constraints (Important)

- No external SaaS uploads allowed
- PHI/PII redaction requirements
- Only approved AI models (no free-tier APIs)
- Primary languages: .NET, Python

---

## Recent Decisions (Jan 19, 2026)

1. Course renamed to "AI Accelerated Software Development"
2. Three distinct phases: Fundamentals (2 wks) → Labs (4 wks) → Applied (4 wks)
3. Labs time commitment: 8-10 hours/week
4. No greenfield/brownfield tracks - everyone works with production codebases
5. "Brownfield" → "Production Codebase" terminology
6. Lab 02 renamed to "Codebase Analysis & Documentation"
7. **Claude approved for Ensemble pilot** — Claude Code CLI is now the primary agentic harness (Copilot CLI content deferred as placeholder for future clients)

---

## Suggested Next Tasks

1. **Build out 3-applied/ content** - The Applied Coaching phase (Weeks 7-10) needs:
   - Coaching session frameworks
   - Progress tracking templates
   - Project selection criteria
   - Capstone deliverable specs
   - Executive ROI readout template

2. **Week 1 critical path** - Minimum viable content for launch

3. **Content production schedule** - Prioritize what to build first

---

## Key Files to Reference

| What | Where |
|------|-------|
| Project context | `CLAUDE.md` |
| Current status | `PROJECT-STATUS.md` |
| Product changes | `products/CHANGELOG.md` |
| Labs syllabus | `products/curriculum/.../2-labs/3-Syllabus/Labs-4-Week-Syllabus.md` |
| Fundamentals syllabus | `products/curriculum/.../1-fundamentals/Fundamentals-2Week-Syllabus.md` |
| Session history | `_project/session-history.md` |
| Today's work | `sessions/2026-01-19-2_product-restructure/SESSION.md` |
