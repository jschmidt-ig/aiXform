# GT Task: Fundamentals Slide Deck Outlines

**Assigned by:** Claude
**Date:** 2026-01-19
**Priority:** High (critical path for pilot launch)

---

## Goal

Create detailed slide outlines for all 20 Fundamentals sessions (Weeks 1-2). These outlines will be used to build the actual presentation decks.

---

## Before You Start

1. **Log your work** in `/Volumes/aiXform/aiXform/COORDINATION.md`
   - Add a row: `2026-01-XX | GT | 🔄 In Progress | Fundamentals slide outlines | Sessions X-Y`

2. **Read these files first:**
   - `GT.md` — Your instruction file
   - `COORDINATION.md` — Work log
   - The syllabus and prompt template (paths below)

---

## Key Files

| File | Purpose |
|------|---------|
| `products/curriculum/ai-accelerated-software-development/foundations/1-fundamentals/Fundamentals-2Week-Syllabus.md` | **The authoritative syllabus** — 20 sessions over 10 days |
| `products/curriculum/ai-accelerated-software-development/foundations/1-fundamentals/Deep-Research-Prompt_Slide-Outlines.md` | **The prompt template** — Use this for each batch |
| `products/curriculum/ai-accelerated-software-development/foundations/1-fundamentals/Fundamentals-Supplemental-Materials.md` | Supplemental reading/videos (for context) |

---

## Workflow

### Step 1: Work in Batches

Don't try to do all 20 sessions at once. Work in batches:

| Batch | Sessions | Day Coverage |
|-------|----------|--------------|
| 1 | Sessions 1-2 | Day 1 |
| 2 | Sessions 3-4 | Day 2 |
| 3 | Sessions 5-6 | Day 3 |
| 4 | Sessions 7-8 | Day 4 |
| 5 | Sessions 9-10 | Day 5 |
| 6 | Sessions 11-12 | Day 6 |
| 7 | Sessions 13-14 | Day 7 |
| 8 | Sessions 15-16 | Day 8 |
| 9 | Sessions 17-18 | Day 9 |
| 10 | Sessions 19-20 | Day 10 |

### Step 2: For Each Batch

1. **Copy the prompt template** from `Deep-Research-Prompt_Slide-Outlines.md`

2. **Set the variables:**
   ```
   SESSIONS_TO_GENERATE: [e.g., "1-2" or "3-4"]
   AUDIENCE_LEVEL: mid/senior software engineers (enterprise)
   TOOLING_CONTEXT: CLI-first later (Claude Code CLI), but Fundamentals is lecture-only
   STYLE: practical, minimal fluff, diagrams where helpful
   SLIDE_DENSITY: 8-12 slides per 20-30 min session
   DEMO_MODE: lecture-only demos (show commands/snippets on slides; no execution required)
   ```

3. **Include the syllabus excerpt** for those sessions (copy from `Fundamentals-2Week-Syllabus.md`)

4. **Run the deep research** and capture the output

5. **Save the output** to:
   ```
   products/curriculum/ai-accelerated-software-development/foundations/1-fundamentals/slide-outlines/
   ```

   Name format: `Sessions-01-02-Slide-Outlines.md`, `Sessions-03-04-Slide-Outlines.md`, etc.

### Step 3: Quality Check Each Batch

Before moving to the next batch, verify:
- [ ] Slide count is reasonable (8-12 per session)
- [ ] Demo examples are lecture-safe (no execution required)
- [ ] Enterprise constraints are respected (no SaaS, approved models, PHI/PII sensitivity)
- [ ] Security framing is present where relevant
- [ ] "Common misconceptions" callouts are included

### Step 4: Build a "Slide Standard" Doc

After Batch 1, note what worked well. Use those patterns as additional constraints for later batches. Save as:
```
products/curriculum/ai-accelerated-software-development/foundations/1-fundamentals/slide-outlines/Slide-Standard-Notes.md
```

---

## Output Structure (Per Session)

Each session outline should include:

1. **Session summary**
   - Title
   - One-sentence purpose
   - 3 learning objectives
   - "If learners only remember 1 thing" line

2. **Slide-by-slide outline**
   - Slide title
   - Key bullets (max 5)
   - Speaker notes
   - Visual/diagram suggestion
   - Time estimate

3. **Demo-in-lecture plan**
   - 1-2 demo moments
   - Command snippets or CLI transcript examples
   - "What to point out" and "what could go wrong" notes

4. **Examples bank**
   - Good example
   - Bad example (and why it fails)
   - Enterprise-safe example

5. **Graphics pack**
   - 2-4 diagram ideas with image prompts
   - Suggested slide placement

6. **Safety & risk callouts**
   - Relevant risks for this session
   - Mitigations to mention
   - Critical safety concepts

---

## Important Context

- **Fundamentals is tool-agnostic** — Teach concepts that apply to ANY AI coding tool
- **Lecture-only** — No code execution during Fundamentals; demos are on-slide examples
- **Enterprise reality** — No external SaaS, approved models only, PHI/PII sensitivity
- **Critical safety topics** — Prompt injection, tool permissioning, least privilege (these are hard-fail on the end test)

---

## When You're Done

1. Update `COORDINATION.md`:
   - Mark your task ✅ Done
   - Note which sessions are complete
   - Add any questions or issues encountered

2. Update `products/CHANGELOG.md` with what you created

3. Leave notes for Claude about:
   - Any sessions that need review
   - Patterns that worked well
   - Suggested improvements to the process

---

## Questions?

If you get stuck or need clarification:
- Note it in `COORDINATION.md` under "Notes / Parking Lot"
- Continue with what you can and flag the blockers
