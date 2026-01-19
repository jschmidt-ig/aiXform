# aiXform

Enterprise AI transformation training — courses and consulting for software development teams.

**First Client:** Ensemble Health Partners — 10-week pilot starting mid-January 2026

---

## Quick Links

| Resource | Description |
|----------|-------------|
| [PROJECT-STATUS.md](PROJECT-STATUS.md) | Current state, what exists, what's needed |
| [COORDINATION.md](COORDINATION.md) | AI work log (Claude + GT coordination) |
| [next-step.md](next-step.md) | Session handoff and startup instructions |
| [products/CHANGELOG.md](products/CHANGELOG.md) | Track all product changes |

---

## Current Course: AI Accelerated Software Development — Foundations

A 10-week program teaching developers to work effectively with AI coding tools.

| Phase | Weeks | Format | Status |
|-------|-------|--------|--------|
| [Fundamentals](products/curriculum/ai-accelerated-software-development/foundations/1-fundamentals/) | 1-2 | 20 sessions (lectures + demos) | Syllabus ✅ Slides 🔄 |
| [Labs](products/curriculum/ai-accelerated-software-development/foundations/2-labs/) | 3-6 | 4 hands-on labs | Syllabus ✅ Instructions ❌ |
| [Applied](products/curriculum/ai-accelerated-software-development/foundations/3-applied/) | 7-10 | Team coaching | Complete ✅ |

**Time commitment:** 8-10 hours/week for all phases

---

## What's Done

### Curriculum Structure
- [Fundamentals syllabus](products/curriculum/ai-accelerated-software-development/foundations/1-fundamentals/Fundamentals-2Week-Syllabus.md) — 20 sessions over 10 days
- [Fundamentals supplemental materials](products/curriculum/ai-accelerated-software-development/foundations/1-fundamentals/Fundamentals-Supplemental-Materials.md) — Reading, videos, exercises
- [Labs syllabus](products/curriculum/ai-accelerated-software-development/foundations/2-labs/3-Syllabus/Labs-4-Week-Syllabus.md) — 4 labs over 4 weeks
- Lab specifications (Lab 01-04)
- [Applied syllabus](products/curriculum/ai-accelerated-software-development/foundations/3-applied/Applied-4Week-Syllabus.md) — Weeks 7-10 coaching
- [Team AI Playbook template](products/curriculum/ai-accelerated-software-development/foundations/3-applied/Team-AI-Playbook-Template.md)
- [ROI Metrics template](products/curriculum/ai-accelerated-software-development/foundations/3-applied/ROI-Metrics-Template.md)
- [Coaching Session Guide](products/curriculum/ai-accelerated-software-development/foundations/3-applied/Coaching-Session-Guide.md)
- [Executive Readout template](products/curriculum/ai-accelerated-software-development/foundations/3-applied/Executive-Readout-Template.md)

### Marketing
- [Foundations landing page](products/marketing/ai-accelerated-software-development/foundations/index.html)
- [Fundamentals brochure](products/marketing/brochures/AI-Accelerated-Software-Development-Fundamentals-Brochure.html)
- [Labs brochure](products/marketing/brochures/AI-Accelerated-Software-Development-Labs-Brochure.html)

### Client Materials
- [Ensemble pitch materials](products/client-materials/ensemble/)

---

## What's Needed

### Critical Path (for pilot launch)
- [ ] **Slide decks for 20 Fundamentals sessions** — GT is assigned, see [task brief](sessions/GT-TASK_Fundamentals-Slide-Decks.md)
- [ ] Recorded video content for Weeks 1-2

### Also Needed
- [ ] Detailed lab instructions with step-by-step guidance
- [ ] Starter code and production codebase examples
- [ ] Safe sandbox environments
- [ ] Assessment answer keys
- [ ] Instructor facilitation guides
- [ ] Applied Phase brochure (Weeks 7-10)
- [ ] Competitive landscape research
- [ ] Case study template for pilot outcomes

---

## Directory Structure

```
aiXform/
├── products/                    # Finished deliverables
│   ├── curriculum/              # Course materials
│   │   └── ai-accelerated-software-development/
│   │       └── foundations/
│   │           ├── 1-fundamentals/   ← Weeks 1-2
│   │           ├── 2-labs/           ← Weeks 3-6
│   │           └── 3-applied/        ← Weeks 7-10
│   ├── marketing/               # Brochures, landing pages
│   └── client-materials/        # Client-specific (Ensemble)
│
├── sessions/                    # Working sessions (YYYY-MM-DD_description)
├── reference/                   # Research, background materials
├── assets/                      # Templates, prompts, images
└── _project/                    # Meta-docs (session history)
```

---

## Business Model

| Tier | Name | Price | Format |
|------|------|-------|--------|
| L1 | Foundations | $300-500/seat | Self-paced, recorded |
| L2 | Practitioner | $2,000-3,000 | 10-week cohort with labs |
| L3 | Enterprise Accelerator | $30,000-50,000 | Team coaching |

---

## Team

| Person | Role |
|--------|------|
| **Dragon** | Founder, executive relationships |
| **Justin** | AI development expert, curriculum |
| **Danny** | Training & instructional design |
| **Scot** | Chief of staff, client management |

### AI Assistants

| Name | Model | Role |
|------|-------|------|
| **Claude** | Claude Code CLI | Lead AI — coordinates project |
| **GT** | GPT 5.2 | Helper — takes assigned tasks |

See [COORDINATION.md](COORDINATION.md) for work log.

---

## Tooling

**Ensemble Pilot:** Claude (approved) — Claude Code CLI as primary agentic harness

**Future Clients:** Some enterprises may be restricted to Windows + GitHub Copilot. Content for Copilot CLI workflows will be developed for those engagements.

**Enterprise Constraints:**
- No external SaaS uploads
- PHI/PII redaction required
- Approved models only
- Primary languages: .NET, Python

---

## Key Decisions

1. Course renamed to "AI Accelerated Software Development" (not "AI SDLC")
2. Three phases: Fundamentals (2 wks) → Labs (4 wks) → Applied (4 wks)
3. Fundamentals is **tool-agnostic** — teaches concepts, not specific products
4. No greenfield/brownfield tracks — everyone works with production codebases
5. 8-10 hours/week for all phases

---

## For New Team Members

1. Read [CLAUDE.md](CLAUDE.md) or [GT.md](GT.md) for AI context
2. Read [PROJECT-STATUS.md](PROJECT-STATUS.md) for current state
3. Check [COORDINATION.md](COORDINATION.md) for active work
4. See [next-step.md](next-step.md) for session conventions
