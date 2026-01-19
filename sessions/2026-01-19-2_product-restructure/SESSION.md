# Session: Product Restructure

**Date:** January 19, 2026
**Focus:** Restructure products with proper course naming and delivery breakdown

## Goal

Update product organization to reflect the actual course structure:
- **Course Name:** AI Accelerated Software Development (not "AI SDLC")
- **Level:** Foundations
- **Three Distinct Deliveries:**
  1. Fundamentals (online course work) - 2 weeks
  2. Labs (hands-on exercises) - 4 weeks
  3. Applied Coaching (guided work on their actual projects) - 4 weeks

## Context

Previously, "Labs" and "Applied" were merged together as an 8-week block. In reality:
- Weeks 1-2: Fundamentals
- Weeks 3-6: Labs
- Weeks 7-10: Applied Coaching

## Changes to Make

1. Rename/restructure `products/curriculum/`:
   - From: `labs-bundle/`, `fundamentals-bundle/`
   - To: Organized under "AI Accelerated Software Development / Foundations"

2. Create `products/CHANGELOG.md` to track product changes

3. Update documentation to reflect new naming

## Outcomes

- Renamed course from "AI SDLC" to "AI Accelerated Software Development"
- Created `products/curriculum/ai-accelerated-software-development/foundations/` structure
- Separated Labs and Applied into distinct 4-week phases
- Created `products/CHANGELOG.md` to track product changes
- Updated `CLAUDE.md` with new course structure and paths
- Updated `PROJECT-STATUS.md` with new structure

## New Directory Structure

```
products/curriculum/
└── ai-accelerated-software-development/
    └── foundations/
        ├── 1-fundamentals/   (Weeks 1-2)
        ├── 2-labs/           (Weeks 3-6)
        └── 3-applied/        (Weeks 7-10)
```

## Extracted To

- `products/CHANGELOG.md` - Product change tracking
- `products/curriculum/ai-accelerated-software-development/` - New structure
