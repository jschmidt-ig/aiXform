# Session: Project Reorganization

**Date:** January 19, 2026
**Focus:** Restructure project for Claude maintainability

## Goal

Create a file/directory structure that Claude can maintain, preserving the session-based workflow while making it easier to find and extract finished work.

## Problems Addressed

- Cryptic session names (`s1`, `s2`) provided no context
- No clear extraction path for finished work products
- Inconsistent internal structure across sessions
- Root level clutter with mixed naming conventions
- `log/` was misleading - these are working sessions, not logs

## Changes Made

### Directory Structure

**Before:**
```
log/s1/, log/s2/, ... log/s8/
w-product/
$$inspire/
integral-dragon->aiXform/
s9-research-classes/
__meta-project-management__/
__meta-work-log__/
```

**After:**
```
sessions/YYYY-MM-DD_description/
products/curriculum/, client-materials/, marketing/
assets/templates/, prompts/, images/
reference/inspiration/, integral-dragon-strategy/, market-research/
_project/session-history.md
```

### Session Renames

| Old | New |
|-----|-----|
| `log/s1/` | `sessions/2026-01-07_market-research/` |
| `log/s2/` | `sessions/2026-01-08_research-consolidation/` |
| `log/s3/` | `sessions/2026-01-10_client-alignment/` |
| `log/s4/` | `sessions/2026-01-11_maturity-model/` |
| `log/s5/` | `sessions/2026-01-12_operational-planning/` |
| `log/s6/` | `sessions/2026-01-13_curriculum-production/` |
| `log/s7/` | `sessions/2026-01-14_visual-assets/` |
| `log/s8/` | `sessions/2026-01-15_final-infographics/` |
| `s9-research-classes/` | `sessions/2026-01-16_research-classes/` |

### Files Created

- `CLAUDE.md` - Root context file for Claude to understand the project
- `SESSION.md` in each session - Documents goals, outcomes, decisions
- `_project/session-history.md` - Detailed session-by-session breakdown

### Files Updated

- `PROJECT-STATUS.md` - Slimmed down to executive summary, updated paths
- `next-step.md` - Updated with new structure and conventions

### Content Extracted to Products

- `products/curriculum/labs-bundle/` - From 2026-01-13 session
- `products/curriculum/fundamentals-bundle/` - From 2026-01-13 session
- `products/marketing/brochures/` - HTML brochures
- `products/marketing/infographics/` - Maturity model visuals
- `products/client-materials/ensemble/` - Client pitch docs

### Directories Removed

- `w-product/` (was empty)
- `__meta-project-management__/` (was empty)
- `__meta-work-log__/` (was empty)
- `$$inspire/` (moved to reference/)
- `integral-dragon->aiXform/` (moved to reference/)

## Conventions Established

### Session Naming
- Format: `YYYY-MM-DD_short-description`
- Multiple sessions same day: `2026-01-19-1_task-one`, `2026-01-19-2_task-two`

### Session Internal Structure
- `SESSION.md` - Summary of goals, outcomes, decisions, extractions
- `_input/` - Materials that came into the session
- `_scratch/` - Working files, experiments
- `_output/` - Deliverables (candidates for extraction)

### Workflow
1. Start session: Create `sessions/YYYY-MM-DD_description/`
2. Work in session using standard subdirs
3. Document outcomes in `SESSION.md`
4. Extract finished work to `products/`
5. Resume later: Tell Claude "Read CLAUDE.md"

## Decisions Made

- Flat session list (no grouping by month/quarter)
- Sessions never span multiple days
- Keep originals in sessions after extracting to products (for reference)
- `_project/` holds project meta-docs to keep PROJECT-STATUS.md concise

## Extracted To

- Conventions documented in `CLAUDE.md`
- Session history in `_project/session-history.md`
