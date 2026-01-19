# Session: Product Restructure & Terminology

**Date:** January 19, 2026
**Focus:** Restructure products, update course naming, fix terminology

## Goals

1. Restructure products with proper course naming
2. Separate Labs (4 weeks) from Applied (4 weeks)
3. Update time commitment to 8-10 hours/week
4. Eliminate greenfield/brownfield distinction
5. Replace "brownfield" with "production codebase"

## Changes Made

### Course Structure
- Renamed course from "AI SDLC" to **"AI Accelerated Software Development"**
- Created three-phase delivery structure under `foundations/`:
  - `1-fundamentals/` (Weeks 1-2) - Online course work, 20 micro-sessions
  - `2-labs/` (Weeks 3-6) - Hands-on lab exercises
  - `3-applied/` (Weeks 7-10) - Guided coaching on real projects

### Labs Updates
- Labs are now 4 weeks (Weeks 3-6), not 8 weeks
- Time commitment updated to 8-10 hours/week (was 6 hours/week)
- 4 core labs (removed optional Lab 05 from main sequence)
- Renamed `10-Week-Syllabus.md` → `Labs-4-Week-Syllabus.md`

### Terminology Changes
- Eliminated greenfield/brownfield track distinction - everyone follows same path
- Replaced "brownfield" with "production codebase" throughout
- Lab 02: "Brownfield Inspection & Documentation" → "Codebase Analysis & Documentation"

### Files Renamed
- `Lab-02-Brownfield-Inspection-DocGen.md` → `Lab-02-Codebase-Analysis-DocGen.md`
- `Brownfield-Worksheet.md` → `Codebase-Analysis-Worksheet.md`

### Files Updated
- `AI-SDLC-Labs-Brochure.html` - 4 weeks, 8-10 hrs, removed tracks section
- `Labs-4-Week-Syllabus.md` - New 4-week structure
- `Student-Schedule-Practitioner.md` - 8-10 hrs/week breakdown
- `Labs-Landing-Page.html` - Updated terminology
- `Lecture-Series.md` - Updated Week 5 title
- `1-Getting-Started/README.md` - Updated file references
- `CLAUDE.md` - Updated course structure
- `PROJECT-STATUS.md` - Updated paths and structure

### New Files
- `products/CHANGELOG.md` - Track product changes
- `products/curriculum/ai-accelerated-software-development/foundations/3-applied/README.md`
- `products/marketing/ai-accelerated-software-development/foundations/` - Course marketing folder

## Directory Structure Created

```
products/
├── CHANGELOG.md
├── curriculum/
│   └── ai-accelerated-software-development/
│       └── foundations/
│           ├── 1-fundamentals/   (Weeks 1-2)
│           ├── 2-labs/           (Weeks 3-6)
│           └── 3-applied/        (Weeks 7-10)
├── client-materials/ensemble/
└── marketing/
    ├── brochures/
    ├── infographics/
    └── ai-accelerated-software-development/foundations/
```

## Decisions Made

- Course name: "AI Accelerated Software Development"
- Level name: "Foundations" (10-week program)
- No track distinction - all learners work with production codebases
- "Brownfield" → "Production Codebase" terminology
- Labs: 4 weeks, 8-10 hrs/week
- Applied: 4 weeks (separate phase with coaching)

## What's Next

1. **Content for 3-applied/**: Build out Applied Coaching phase materials (Weeks 7-10)
2. **Gap Analysis**: Map specs to actual content needed for delivery
3. **Week 1 Critical Path**: Identify minimum content for launch
4. **Environment Setup**: Sandbox repos, lab infrastructure
