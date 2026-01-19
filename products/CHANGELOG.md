# Products Changelog

All notable changes to product structure and content.

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
  - **1-fundamentals/** (Weeks 1-2): Online course work, 20 micro-sessions
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
