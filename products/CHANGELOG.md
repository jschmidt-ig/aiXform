# Products Changelog

All notable changes to product structure and content.

---

## 2026-01-19 (Applied Coaching Phase Content)

### Added
Complete Applied phase content for Weeks 7-10:

- `3-applied/Applied-4Week-Syllabus.md` — Week-by-week structure, objectives, coaching model
- `3-applied/Team-AI-Playbook-Template.md` — Template for team AI rules, practices, workflows
- `3-applied/ROI-Metrics-Template.md` — Baseline/final metrics, ROI calculation, qualitative assessment
- `3-applied/Coaching-Session-Guide.md` — Facilitation guide with weekly agendas, discussion prompts, handling common situations
- `3-applied/Executive-Readout-Template.md` — Slide-by-slide template for leadership presentation

### Updated
- `3-applied/README.md` — Complete overview with document index

### Key Concepts
- **Three objectives:** Apply to real projects, customize workflows, establish new ways of working
- **Key deliverable:** Team AI Playbook (team's documented rules and practices)
- **Coaching model:** Team sessions + 1:1s + office hours
- **Facilitation philosophy:** Coach as facilitator, not prescriber

---

## 2026-01-19 (Fundamentals Supplemental Materials)

### Added
- `1-fundamentals/Fundamentals-Supplemental-Materials.md` - Complete tool-agnostic guide with:
  - Pre-session and post-session materials for all 10 days
  - Generic reading assignments (learners find current articles)
  - Videos (3Blue1Brown transformer explanation)
  - OWASP LLM security reading (required)
  - Reflection exercises and practical activities
  - Time breakdown showing ~10.5 hrs/week total
  - Instructor notes for cohort customization

### Updated
- `1-fundamentals/Fundamentals-2Week-Syllabus.md` - Added tool-agnostic note and time commitment section
- `CLAUDE.md` - Added product note about Fundamentals being tool-agnostic

### Product Note
> Fundamentals (Weeks 1-2) is intentionally **tool-agnostic**. It teaches concepts and mental models that apply to ANY AI coding tool. Instructors may demo various tools, but it's not a tutorial on any specific product. Tool-specific skills come in Labs/Applied.

---

## 2026-01-19 (Fundamentals Time Commitment)

### Changed
- Updated Fundamentals from 4 hrs/week to 8-10 hrs/week (consistent with Labs and Applied)
- Added "supplemental materials" as gap item - need assigned reading/videos to fill additional hours

### Files Updated
- `PROJECT-STATUS.md`, `next-step.md` - added gap item, updated time table
- `products/marketing/ai-accelerated-software-development/foundations/index.html`
- `products/marketing/brochures/AI-Accelerated-Software-Development-Fundamentals-Brochure.html`

---

## 2026-01-19 (Terminology Update - Micro-sessions)

### Changed
- Replaced "micro-sessions" terminology throughout with "sessions"
- Fundamentals now described as "20 sessions (lectures and demonstrations)"
- Updated project docs, curriculum, and marketing materials

### Files Updated
- `CLAUDE.md`, `PROJECT-STATUS.md`, `next-step.md`
- `products/CHANGELOG.md`
- `products/curriculum/.../1-fundamentals/Fundamentals-2Week-Syllabus.md`
- `products/curriculum/.../1-fundamentals/Marketing-Page_Fundamentals.html`
- `products/curriculum/.../2-labs/3-Syllabus/Labs-4-Week-Syllabus.md`
- `products/marketing/ai-accelerated-software-development/foundations/index.html`
- `products/marketing/brochures/AI-Accelerated-Software-Development-Fundamentals-Brochure.html`

---

## 2026-01-19 (Brochures Update)

### Changed
- Updated Fundamentals brochure:
  - Renamed "AI SDLC" → "AI Accelerated Software Development"
  - Added "Phase 1 of 3" header
  - Updated Session 13 to reference Claude Code CLI
  - Fixed hours display and phase references
- Updated Labs brochure:
  - Added "Phase 2 of 3" header
  - Fixed "Two Tracks" → "Production Codebases" (tracks eliminated)
  - Fixed prerequisite to reference new Fundamentals name
  - Fixed week numbers (Labs are weeks 3-6, not arbitrary)
  - Changed "Capstone" section to "What's Next: Applied Phase"

### Renamed Files
- `AI-SDLC-Fundamentals-Brochure.html` → `AI-Accelerated-Software-Development-Fundamentals-Brochure.html`
- `AI-SDLC-Labs-Brochure.html` → `AI-Accelerated-Software-Development-Labs-Brochure.html`

---

## 2026-01-19 (Foundations Marketing Page)

### Added
- `products/marketing/ai-accelerated-software-development/foundations/index.html` - Landing page for full 10-week Foundations program
  - Overview of 3-phase structure (Fundamentals → Labs → Applied)
  - Value proposition for enterprises
  - Program outcomes and metrics
  - Claude Code CLI as primary tooling
  - Enterprise constraints and off-network coaching model

---

## 2026-01-19 (Tooling Update)

### Changed
- **Claude approved for Ensemble pilot** — Claude Code CLI is now the primary agentic harness
- Removed "Windows + GitHub Copilot" as the primary constraint for Ensemble
- Added placeholder notes for future clients who may be restricted to Copilot CLI

### Updated Files
- `CLAUDE.md` - Added Tooling section
- `PROJECT-STATUS.md` - Added Tooling section, updated constraints
- `next-step.md` - Added Tooling section, added to Recent Decisions
- `README.md` - Updated tooling paragraph
- `1-fundamentals/Fundamentals-2Week-Syllabus.md` - Updated audience and Session 13
- `2-labs/1-Getting-Started/README.md` - Updated tooling assumptions
- `client-materials/ensemble/DevDatta-pitch-questions__Ensemble_AI_SDLC_Enablement_10_Week_Pilot.md` - Added approved tooling section, resolved tool approval risk

---

## 2026-01-19 (Terminology Update)

### Changed
- Eliminated greenfield/brownfield track distinction - all learners follow same path
- Replaced "brownfield" terminology with "production codebase" throughout
- Lab 02 renamed: "Brownfield Inspection & Documentation" → "Codebase Analysis & Documentation"

### Renamed Files
- `Lab-02-Brownfield-Inspection-DocGen.md` → `Lab-02-Codebase-Analysis-DocGen.md`
- `Brownfield-Worksheet.md` → `Codebase-Analysis-Worksheet.md`

### Updated Files
- `AI-SDLC-Labs-Brochure.html` - Removed tracks section, updated Lab 02 references
- `Labs-4-Week-Syllabus.md` - Removed tracks section, updated terminology
- `Labs-Landing-Page.html` - Updated badge and Lab 02 name
- `Lecture-Series.md` - Updated Week 5 title
- `1-Getting-Started/README.md` - Updated file references

---

## 2026-01-19 (Labs Content Update)

### Changed
- Updated Labs phase to 4 weeks (Weeks 3-6), not 8 weeks
- Updated learner time commitment to 8-10 hours/week (was 6 hours/week)
- Renamed `10-Week-Syllabus.md` to `Labs-4-Week-Syllabus.md`
- Updated brochure to reflect 4 labs, 4 weeks, 8-10 hrs/week
- Removed references to Applied phase content from Labs materials

### Files Updated
- `products/marketing/brochures/AI-SDLC-Labs-Brochure.html`
- `products/curriculum/.../2-labs/3-Syllabus/Student-Schedule-Practitioner.md`
- `products/curriculum/.../2-labs/3-Syllabus/Labs-4-Week-Syllabus.md` (renamed)

---

## 2026-01-19 (Product Restructure)

### Changed
- Renamed course from "AI SDLC" to "AI Accelerated Software Development"
- Restructured curriculum into three distinct delivery phases:
  - **1-fundamentals/** (Weeks 1-2): Online course work, 20 sessions
  - **2-labs/** (Weeks 3-6): Hands-on lab exercises
  - **3-applied/** (Weeks 7-10): Guided coaching on learner's actual projects
- Previously "Labs" and "Applied" were merged as 8-week block; now separated into 4 weeks each

### Added
- `products/CHANGELOG.md` - This file
- `products/curriculum/ai-accelerated-software-development/foundations/` - New structure

### Directory Structure
```
products/
├── curriculum/
│   └── ai-accelerated-software-development/
│       └── foundations/
│           ├── 1-fundamentals/   (Weeks 1-2)
│           ├── 2-labs/           (Weeks 3-6)
│           └── 3-applied/        (Weeks 7-10)
└── marketing/
    ├── brochures/           (existing brochures)
    ├── infographics/        (existing infographics)
    └── ai-accelerated-software-development/
        └── foundations/     (course-specific marketing)
```
