# GT Context: Ensemble Proposal Package (R2)

**Purpose:** Create a polished, sales-focused proposal package for DevDatta Halbe at Ensemble Health Partners.

**Tone:** Professional, confident, sales/marketing-focused. This should feel polished and fresh—not a dry technical document.

---

## Your Assignment

Create **three artifacts** in order:

### Artifact 1: AI Transformation Strategy Overview (1-2 page infographic/visual document)
A high-level piece about AI transformation strategy in general and aiXform's approach. This sets the strategic context before diving into the specific course.

**Should cover:**
- Why AI-accelerated software development matters now
- The maturity progression (from autocomplete to agentic workflows)
- aiXform's philosophy: practical, measurable, enterprise-safe
- How this connects to broader AI transformation goals

### Artifact 2: 10-Week Pilot Proposal (Sales-focused)
The core proposal document for the AI Accelerated Software Development pilot.

**Must answer:**
- What are they getting?
- What are the benefits?
- How do we measure success?
- How much does it cost?
- How long does it take?

**Key selling points to emphasize:**
- First pilot uses hourly billing (simpler, cheaper, allows customization)
- We show success → roll out to rest of organization
- Show future pricing so they understand the value
- We have a solid course outline already (show confidence)

### Artifact 3: Product Brochure (1-2 page, nicely formatted)
A visual, marketing-style overview of the AI Accelerated Software Development - Foundations program. Think "leave-behind" quality.

---

## Client Context

### Who is DevDatta Halbe?
- **Title:** SVP, Product Engineering at Ensemble Health Partners
- **Role:** Executive sponsor for the AI initiative
- **What he needs to see:** Clear value proposition, measurable outcomes, realistic costs, confidence that we know what we're doing

### About Ensemble Health Partners
- Healthcare revenue cycle management company
- Enterprise environment with security constraints
- Primary languages: .NET, Python
- **Claude has been approved** for the pilot (Claude Code CLI is the primary agentic harness)
- No external SaaS uploads, PHI/PII redaction required, approved models only

### What Ensemble wants
- **AI-accelerated software delivery** — ship software faster and safer
- **Repeatable, safe workflows** — not just "playing with AI"
- **Measurable outcomes** — prove ROI to leadership
- **Scalable model** — pilot first, then roll out to broader org

---

## About aiXform

**Who we are:** AI transformation training company targeting enterprise software development (spin-out from Integral Dragon consulting)

**Our approach:**
- Practical, not theoretical
- Enterprise-safe from day one
- Measurable outcomes, not just "training"
- We create reusable courseware that scales

**Our philosophy:**
- AI SDLC is a multiplier — faster software delivery accelerates all AI initiatives
- Agents need tools → Tools require software → Software velocity is the unlock
- Start with a small cohort, prove impact with metrics, then scale

---

## The Course: AI Accelerated Software Development — Foundations

### Program Structure (10 weeks)

| Phase | Weeks | Format | Focus |
|-------|-------|--------|-------|
| **Fundamentals** | 1-2 | 20 sessions (lectures + demos) | Mental model for AI-assisted development |
| **Labs** | 3-6 | 4 hands-on labs | Practical skills in safe environments |
| **Applied** | 7-10 | Team coaching | Real projects with measurable outcomes |

---

### Phase 1: Fundamentals (Weeks 1-2)

**Format:** 20 sessions, each 20-30 minutes. Lecture + demos. No coding required.

**What learners will be able to do after Fundamentals:**
1. Explain what an LLM does at inference time and what it cannot do (no in-session learning, no durable memory)
2. Understand training vs inference and why "crystallized intelligence" matters
3. Master context windows and how context assembly affects quality and safety
4. Distinguish chatbot UI vs raw API usage vs agentic harnesses (IDE, CLI, cloud agent)
5. Explain agentic workflows (plan-act-observe-reflect) and where they break in practice
6. Understand tool calling, MCP, and when each approach is justified
7. Apply safe judgment on tool permissioning and least privilege principles
8. Recognize and mitigate prompt injection attacks

**Session Overview (10 days, 2 sessions per day):**

| Day | Session A | Session B |
|-----|-----------|-----------|
| 1 | Course Orientation | Tooling & Enterprise Constraints |
| 2 | LLMs & Tokens | Transformer Mental Model |
| 3 | Training vs Inference | Context Window & Memory |
| 4 | Prompting Fundamentals | Chatbot vs Raw Model Call |
| 5 | Prompt Contracts & Output Schemas | Context Engineering Workshop |
| 6 | Agents vs Workflows | Harness Taxonomy |
| 7 | Agentic Coding Method | Model Mixing & Selection |
| 8 | Tool Calling | MCP vs API Calls |
| 9 | Securing Tool Calls | Prompt Injection |
| 10 | Security Scenarios Lab | Integrated Capstone + Recap |

**Assessment:** End-of-module test (10 questions, 12-15 min) with critical safety pass/fail gates on:
- Prompt injection recognition
- Least-privilege tool permissioning
- Untrusted input handling

**Design note:** Fundamentals is intentionally tool-agnostic — teaches concepts that apply to any AI coding tool. Instructors may demo various tools, but it's not a tutorial on any specific product. This content can be recorded and reused for broader rollout.

---

### Phase 2: Labs (Weeks 3-6)

**Format:** 4 structured labs. Each week: ~2 hrs lecture + 5-6 hrs hands-on + 1-2 hrs review.

**Lab 01: API Foundations (Week 3)**
Build a minimal API in a safe sandbox environment. Focus on clean workflow.
- **Deliverables:** API contract, plan-mode output, implementation (2+ endpoints), unit tests (4+), PR narration + permissions note
- **Skills:** Plan mode, task decomposition, permissions boundaries, diff-first development, PR narration

**Lab 02: Codebase Analysis & Documentation (Week 4)**
Inspect a production codebase safely (read-only), generate usable documentation, create risk-ranked backlog.
- **Deliverables:** Architecture README, ADR v1, dependency & boundary map, risk-ranked backlog (top 10 safe PR candidates)
- **Skills:** Safe repo inspection, hot spot identification, actionable documentation

**Lab 03: Testing & Coverage Acceleration (Week 5)**
Baseline measurement, high-ROI test selection, coverage delta reporting.
- **Deliverables:** Coverage baseline, test plan, new tests (8+), coverage delta report, refactoring notes
- **Skills:** Baseline measurement, high-ROI test targeting, human review loop for AI-generated tests

**Lab 04: Observability, Security & Compliance (Week 6)**
Instrument service with observability, run security/compliance drill.
- **Deliverables:** Structured logging implementation, correlation ID propagation, runbook, redaction checklist, prompt injection drill findings + mitigations
- **Skills:** Structured logging, operational handoff, prompt injection defense in practice

**Assessment Rubrics:**
- **PR Rubric:** Clear summary, explained "why", risk assessment, testing documented, follow-ups identified
- **Tests Rubric:** Readable, deterministic, edge cases covered, maintainable, coverage targets met
- **Docs Rubric:** Actionable for new engineers, accurate, risks identified, run/build steps verified
- **Prompts Rubric:** Clear constraints, output contract specified, no sensitive data, reproducible

---

### Phase 3: Applied (Weeks 7-10)

**Format:** Team coaching + 1:1 sessions + office hours. 2-3 teams per cohort.

**Objectives:**
1. Apply tools to real projects — take lab skills to production codebases
2. Customize AI workflows — adapt techniques to specific context
3. Establish new ways of working — define team practices and governance

**Week-by-Week:**

| Week | Focus | Key Activities |
|------|-------|----------------|
| 7 | Transition & Baseline | Identify focus areas, capture baseline metrics, document current workflows |
| 8 | Workflow Design | First AI-assisted PRs, draft Team AI Playbook |
| 9 | Iteration & Refinement | Mid-point review, refine playbook, prepare capstone |
| 10 | Capstone & Readout | Final PRs, ROI metrics compilation, executive presentation, sustainability planning |

**Coaching Structure:**
- Weekly team sessions: 2 hrs/week (structured, facilitated)
- 1:1 coaching: As needed (specific challenges, role questions)
- Office hours: 2 hrs/week (open drop-in)

**Key Deliverables:**
- **Team AI Playbook** — Team's documented rules, practices, and workflows for AI-assisted development
- **Capstone PRs** — Real PRs demonstrating AI-assisted workflow on production code
- **ROI Metrics** — Before/after measurements for leadership
- **Executive Readout** — Summary presentation of outcomes and recommendations

**Good Focus Areas for Applied:**
- Add test coverage to an under-tested module
- Refactor a well-understood but messy component
- Generate/update documentation for a service
- Implement a small, well-defined feature
- Fix a backlog of minor bugs

**Avoid:**
- Critical path production changes
- Security-sensitive code without proper review
- Large architectural changes
- Anything requiring extensive approvals

---

## Pricing Model

### For This Pilot: Hourly Billing (Recommended)

Ensemble already has an approved contract vehicle for hourly billing. For the first pilot, we propose billing under that contract.

**Benefits:**
- Minimizes procurement friction
- Allows customization during delivery
- Actually cheaper than list pricing for first run
- Simple: bill only actual time spent

**Estimated instructor effort (first pilot):** 150-210 hours total

### List Pricing (For Future Rollouts)

Once the pilot proves successful, future cohorts use list pricing:

| Component | Price |
|-----------|-------|
| Fundamentals | $500/seat |
| Labs | $2,500/seat |
| Applied | $20,000/cohort |

**Program total formula:** `C × ($3,000 × N + $20,000)` where C = cohorts, N = seats per cohort

**Example pricing:**
| Scenario | Cohorts | Seats/Cohort | Total |
|----------|---------|--------------|-------|
| Small pilot | 1 | 15 | $65,000 |
| Full cohort | 1 | 20 | $80,000 |
| Department rollout | 3 | 15 | $195,000 |
| Large rollout | 3 | 20 | $240,000 |

**Why show this:** DevDatta should understand the value they're getting with hourly billing, and see what broader rollout would cost.

---

## Time Commitment

### For Learners
- **Weekly:** 8-10 hours/week (all phases)
- **Total program:** 80-100 hours over 10 weeks

**Breakdown by phase:**

| Phase | Lectures/Sessions | Hands-on/Lab | Review/Support |
|-------|-------------------|--------------|----------------|
| Fundamentals | ~8-10 hrs | — | Supplemental reading ~8-10 hrs |
| Labs | ~2 hrs/week | 5-6 hrs/week | 1-2 hrs/week |
| Applied | — | Project work | 4+ hrs coaching/office hours |

### For Organization
- Identify 1-3 teams, ~15 participants (cap 20)
- Protect participant time (8-10 hrs/week)
- Provide access to tooling and safe lab environment
- Provide KPI sources for measurement

### Trainer Time (For Reference)
- **First pilot (content creation):** ~20-30 hrs/week average
- **Steady-state (reusable content):** ~8 hrs/week

---

## Measurable Outcomes

### What we measure:

**Delivery:**
- PR throughput and time-to-merge
- Cycle time (ticket → merge)
- PR size

**Quality:**
- Test coverage delta
- Review iteration count / reopen rate
- Documentation completeness

**Adoption:**
- Usage rate (self-report + signals)
- Developer satisfaction (survey at Week 2, 6, 10)

### Measurement timeline:
- **Week 1:** Baseline capture
- **Week 6:** Mid-point check (directional)
- **Week 10:** Final results + narrative

### Target outcomes by Week 10:
- Teams consistently using agentic coding workflow
- At least one high-signal improvement per team (capstone PRs)
- Repeatable, safe workflow established (Team AI Playbook)
- ROI data ready for executive presentation
- Replicable model for other teams

---

## AI SDLC Maturity Model

This is our framework for understanding the progression from basic AI assistance to full agentic workflows.

### The 5 Levels

| Level | Name | Human Role | AI Role | Unit of Work |
|-------|------|------------|---------|--------------|
| 1 | Autocomplete Assist | Author | Completer | Snippets, lines |
| 2 | Supervised Agent Coding | Pair + Supervisor | Implementer (supervised) | Files, small tasks |
| 3 | PR-Submitting Agent | Reviewer + Approver | PR author | Full stories |
| 4 | Multi-Agent Orchestration | Lead + Integrator | Specialists (parallel) | Features |
| 5 | Agent Org / Hierarchical Team | Manager + Governor | Decision-making org | Milestones, epics |

### The Key Insight
- **This pilot targets Level 2-3** — the practical "high-ROI" zone
- Most teams are stuck at Level 1 (autocomplete)
- Moving to supervised/delegated agentic coding unlocks significant productivity gains
- Foundation for future progression to Levels 4-5

### Productivity Multipliers (Indicative ranges)
- L1 (Autocomplete): ~1.05× – 1.3×
- L2 (Supervised agent): ~1.2× – 2×
- L3 (PR agent): ~1.5× – 4×
- L4 (Multi-agent): ~2× – 8×
- L5 (Agent org): ~3× – 15×

### What changes at each level:

**Human role shifts:** Author → Pair + Supervisor → Reviewer → Lead + Integrator → Manager + Governor

**Quality signal shifts:**
- L1-2: Correctness ensured by human inspection
- L3: Shifts toward PR review + tests
- L4-5: Higher-level signals (CI gates, functional checks, eval harnesses)

---

## Key Messages to Emphasize

### 1. "Agents need tools. Tools require software."
Ensemble's AI goals depend on the org's ability to ship software faster. AI SDLC is a multiplier across all AI initiatives.

### 2. "Practical, not theoretical"
This isn't just training — participants produce real artifacts, work on real projects, and deliver measurable outcomes.

### 3. "Start small, prove impact, then scale"
The pilot is designed to create reusable courseware and internal champions for broader rollout.

### 4. "Enterprise-safe from day one"
Security constraints are built into the curriculum: least privilege, safe permissioning, prompt injection awareness. Critical safety assessment is a gate.

### 5. "You get a playbook, not just knowledge"
Teams leave with a documented "how we work" playbook they own and believe in.

### 6. "We have the course outlined and ready"
Show confidence — 20 sessions detailed, 4 labs specified, coaching framework documented. This isn't vaporware.

---

## Decisions Needed (to include in proposal)

By end of Week 1, Ensemble needs to decide:
1. **Cohort selection** — 1-3 teams, participant list (~15, cap 20)
2. **Environment choice** — Cloud lab (recommended) vs dev containers vs WSL
3. **Tool access** — Claude Code CLI usage + logging policy
4. **Data handling rules** — What can/can't enter prompts; redaction expectations
5. **KPI access** — ADO, dashboards, or manual sampling

---

## Success Criteria

### For Teams:
- Completed Team AI Playbook they believe in
- Demonstrated AI-assisted workflow on real code
- Clear understanding of when/how to use AI
- Confidence to continue after pilot ends

### For Organization:
- Measurable ROI data for leadership
- Replicable model for other teams
- Identified champions for broader rollout
- Clear recommendations for next steps

---

## What You're Creating (Summary)

1. **AI Transformation Strategy Overview** — Strategic context, our approach, why this matters (1-2 page visual)
2. **10-Week Pilot Proposal** — What they get, benefits, measurement, cost, timeline (sales-focused)
3. **Product Brochure** — Visual, polished, leave-behind quality (1-2 page)

**Remember:** Sales/marketing tone. Polished and fresh. Show confidence in our course outline. Make DevDatta feel confident that we know what we're doing and can deliver measurable results.
