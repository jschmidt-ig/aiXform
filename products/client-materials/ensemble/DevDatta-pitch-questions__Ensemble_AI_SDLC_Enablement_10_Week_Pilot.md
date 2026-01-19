# Ensemble AI SDLC Enablement (10‑Week Pilot)  
**Prepared for:** Ensemble (Sponsor: DevData)  
**Prepared by:** Integral Brain / AIXform (AI SDLC Enablement)  
**Purpose:** Align on the *why*, *what*, and *how* for a 10‑week program that brings 1–3 development teams up to speed on **AI‑assisted / agentic software delivery (AI SDLC)**—including the tooling, security model, workflow changes, and measurable success criteria.

---

## 1) Executive summary

Ensemble’s opportunity in AI is not only “agents running business processes,” but **the organization’s ability to ship software, tools, and APIs faster and more safely**—because those building blocks are what agents will rely on.

### Our delivery model (three layers)

This engagement is intentionally structured around three delivery layers that also scale to the broader organization:

1. **Courseware (recorded fundamentals):** reusable video modules + worksheets + templates.  
   *Weeks 1–2 are designed to be recorded and repackaged for broader rollout.*
2. **Instructor-led labs:** live, hands-on workshops built around example projects and repeatable workflows (Weeks **3–6**).
3. **Direct coaching on real work:** apply the workflow to Ensemble’s assigned projects with measurable outcomes and executive-ready reporting (Weeks **7–10**).

This 10‑week pilot is designed to:


1. **Establish safe AI development enablement** (tool access, guardrails, environment) under enterprise security constraints.  
2. **Train teams on agentic coding workflows** (beyond “autocomplete Copilot”), using hands‑on labs and example projects.  
3. **Apply the workflow directly to real Ensemble projects** in the final phase, with coaching and measurable productivity/quality deltas.  
4. **Produce reusable courseware** (recorded Weeks 1–2 content) to accelerate rollout to the broader org.

**Cohort recommendation:** 1–3 teams, **target 15 participants** (cap ~20) for the first run.

---

## 2) Where this fits in Ensemble’s AI strategic vision

### The strategic thesis

Ensemble’s AI strategy requires three reinforcing capabilities:

1. **Infrastructure for rapid, safe AI deployment**  
   - We saw in earlier work (e.g., MR Upload) that infrastructure + deployment friction is a primary limiter.  
   - That motivates the push toward **Enclave**: managed environments and infrastructure optimized for rapid AI‑based deployment.

2. **AI‑accelerated software delivery (AI SDLC)**  
   - Agentic workflows for *software development* are now the most practical “high‑ROI” agent use case: they can dramatically increase delivery speed and quality when paired with engineering guardrails and review discipline.  
   - This program focuses here: making AI SDLC repeatable and safe.

3. **Agentic business process execution** (future-facing)  
   - As software/tooling velocity rises, Ensemble can more rapidly build the APIs and internal systems that make business-process agents reliable at scale.

### Why we’re starting with AI SDLC enablement

- **Agents need tools. Tools require software.**  
  To scale business agents, Ensemble needs to ship and evolve tools/APIs quickly.
- **AI SDLC is a multiplier.**  
  Improving the SDLC increases the org’s overall ability to support AI workloads and agent initiatives.

---

## 3) Program goals and outcomes

### Program goals
By the end of Week 10, the cohort will:

- Use an **agentic coding workflow** consistently (planning → implementation → testing → review → safe PR).  
- Have an **approved, repeatable environment** for AI‑assisted development (or an equivalent policy-backed workflow).  
- Demonstrate at least **one concrete delivery improvement** on a real project (capstone) backed by metrics.

### Expected outcomes (measurable)
We will target improvements in:

- **Delivery speed / flow**
  - PR throughput and time-to-merge
  - Cycle time (idea/ticket → code → test → merge)
- **Quality / confidence**
  - Test coverage or test volume increases (where meaningful)
  - Reduced rework (e.g., PR reopen rate, review iterations)
- **Engineering enablement**
  - Developer adoption rate (how often AI workflow is used)
  - Developer satisfaction (simple survey / NPS-like score)

---

## 4) Delivery model: 10 weeks in 3 phases

### Phase overview

| Phase | Weeks | Delivery mode | Primary focus | Key outputs |
|---|---:|---|---|---|
| **Phase 1** | 1–2 | Live instruction + recorded content | AI fundamentals + agentic coding foundations + enablement kickoff | Recorded modules, baseline metrics, environment decision + plan |
| **Phase 2** | 3–6 | Instructor-led labs (hands-on) | Agentic coding techniques via example projects + workflow integration | Lab artifacts, “how we work” playbook draft, initial sandbox PRs |
| **Phase 3** | 7–10 | Coached implementation on real projects | Apply workflow + tools to assigned projects; measure and report improvements | Capstone PRs, KPI deltas, rollout plan + recommendations |

---

## 5) Enablement (tools, access, and safe environments)

A successful pilot depends on early alignment on **how developers will safely access AI tooling**.

### Approved Tooling (Updated Jan 2026)

**Claude has been approved for the Ensemble pilot.** The primary agentic harness will be **Claude Code CLI**.

This simplifies the enablement workstream significantly—we can proceed with Claude-based workflows from Week 1.

### Environment options (to pick with DevData / Dave Dotta)

**Option A — Isolated cloud lab environment (recommended for enterprise constraints)**
- A self-contained development environment in Ensemble's cloud subscription.
- Pros: strongest isolation and governance; easiest to standardize across teams.
- Cons: requires infra setup and approvals.

**Option B — Dev containers on developer machines**
- Docker-based dev containers for a controlled local lab.
- Pros: fast to start; reproducible; good for workshops.
- Cons: local machine variability; security review may be needed.

**Option C — Windows + WSL-based development setup**
- For Windows-heavy teams; WSL provides a consistent Linux-like environment.
- Pros: practical where Docker is constrained.
- Cons: still requires clear policy + support.

### Enablement workstream outputs (Weeks 1–4)
- Tooling access approach (Claude Code CLI, logging policy)
- Usage rules (what data can/can't be used; redaction guidance)
- A "safe lab" repo + workflow that does **not** require production access
- Escalation path for approvals (security, architecture, platform owners)

---

## 6) Participant time requirements and weekly cadence

We’ll design the cadence to be predictable and sustainable.

### Recommended time allocation (pilot cohort)
- **Average:** ~**6 hours/week** of structured time (training + labs + coaching), plus project work in Weeks 7–10 that should overlap with normal delivery workstreams.
- **Cadence principle:** short, repeatable blocks rather than “all-day” sessions.

### Example weekly cadence (can be adapted)
- **Mon:** Weekly module (≈1 hour)  
- **Tue:** Lab / workshop (≈2 hours)  
- **Wed:** Review + office hours / Q&A (≈1 hour)  
- **Thu:** Lab / workshop (≈2 hours)  
- **Fri:** Submission + retrospective (≈1 hour)

---

## 7) Draft week-by-week outline (initial)

> This is intentionally structured so Weeks 1–2 can be recorded and reused as courseware.

| Week | Theme | What we do | Artifacts produced |
|---:|---|---|---|
| 1 | AI fundamentals + safe use kickoff | LLM fundamentals, prompt hygiene, “safe AI SDLC loop,” baseline metrics, enablement discovery | Baseline metrics snapshot + initial guardrails draft |
| 2 | Agentic coding foundations | Agentic workflow: task decomposition → plan → diff → PR narrative; intro labs | “Agentic workflow checklist” + first sandbox PR |
| 3 | Lab sprint 1: feature delivery | Example project: agent builds most code; engineer reviews; focus on correct scoping | PR(s) + review notes + “what changed/why/how tested” template |
| 4 | Lab sprint 2: testing acceleration | AI-assisted test planning and generation, coverage uplift strategies | Test plan + coverage delta report |
| 5 | Lab sprint 3: docs + architecture extraction | Turn code into usable docs (ADRs/runbooks), minimize drift | ADR + runbook + architecture notes |
| 6 | Workflow integration | Apply the workflow to the team’s real SDLC (branching, PR rules, review norms) | Team AI SDLC playbook v1 |
| 7 | Project coaching 1 | Pick target project tickets; coach “safe PR” strategy and execution | 1–2 “safe PRs” toward real repo |
| 8 | Project coaching 2 | Expand to higher-impact tickets; add quality gates where possible | PR(s) + quality checklist |
| 9 | Project coaching 3 | Hardening: testing, docs, rollout guidance; capture metrics mid/end | KPI delta draft + rollout proposal |
| 10 | Capstone + executive readout | Finalize deliverables; present results and next 90‑day plan | Capstone package + final KPI delta report |

---

## 8) Rollout strategy beyond the pilot

The pilot is designed to create **reusable assets** and **internal champions**.

### Rollout mechanics
1. **Record Weeks 1–2** as enterprise-ready courseware  
   - This becomes a repeatable on-ramp for additional teams.
2. **Create champions** from the pilot cohort  
   - Identify 2–4 “AI SDLC champions” who can help lead future cohorts.
3. **Expand via a tiered rollout**
   - Broad org: courseware + lightweight support  
   - Target teams: instructor-led labs  
   - High-impact teams: coached implementation (similar to Phase 3)

### Cultural adoption
- Start with a small cohort, prove impact with metrics, then scale.
- Make it safe: clear rules, clear environments, and repeatable workflows.

---

## 9) Success criteria and reporting

### Measurement approach (simple and defensible)
- **Week 1:** capture baseline  
- **Week 6:** mid-point check (directional)  
- **Week 10:** final results + narrative

### KPI menu (initial)
| KPI | Why it matters | How we measure |
|---|---|---|
| Cycle time (ticket → merge) | Measures delivery acceleration | Sample of comparable tickets before/after |
| PR throughput | Proxies team output flow | PR counts, PR size, merge frequency |
| Review iteration count | Shows quality + clarity | PR comment threads / reopen rate |
| Test coverage delta | Improves confidence and changeability | Coverage or test count deltas |
| Docs completeness | Reduces onboarding and change risk | Presence/quality of ADRs, runbooks |
| Adoption rate | Indicates real behavior change | Self-report + tool usage signals (where available) |
| Dev satisfaction | Predicts sustainability | Survey at Week 2, 6, 10 |

---

## 10) Decisions needed (early)

To keep the pilot moving smoothly, we recommend locking these by end of Week 1:

1. **Cohort selection:** which 1–3 teams and participant list  
2. **Environment choice:** lab environment vs dev containers vs WSL  
3. **Tool access:** approved models + how developers access them  
4. **Security rules:** what data classes can/can’t be used; redaction expectations  
5. **Metrics access:** which KPI sources we can use (ADO, internal dashboards, manual sampling)

---

## 11) Risks and mitigations (pilot)

| Risk | What could happen | Mitigation |
|---|---|---|
| ~~Tool approvals take longer than expected~~ | ~~Training stalls early~~ | ✅ **Resolved:** Claude approved for pilot |
| Security constraints limit real-repo usage | Hard to do hands-on | Sandbox-first approach; shift production codebase work to read-only analysis until allowed |
| Cohort too large | Reduced coaching quality | Keep first cohort at ~15; cap at ~20 |
| Not enough time protected | Low adoption / poor outcomes | Set expectations upfront: predictable weekly cadence; manager support |
| "AI = autocomplete" mindset | Underuse of agentic workflows | Explicitly teach maturity progression + safe PR practices + review discipline |

---

## Appendix A — AI SDLC progression model (for infographic)

**Goal:** visually communicate how AI usage evolves from “helper” to “agent” to “engineered agent systems.”

### Level 1 — Code Assist (Autocomplete)
- AI suggests snippets while developer writes most code.
- Primary value: speed for small edits and boilerplate.
- Mental model: **Developer in control; AI is a smart autocomplete.**

### Level 2 — Agentic Coding (pair-programming with an AI agent)
- AI agent produces the majority of code changes from a task brief.
- Engineer supervises: sets constraints, reviews diffs, runs tests, merges PRs.
- Mental model: **AI drives; engineer steers and verifies.**

### Level 3 — Engineered Agent Systems (AI as a scalable “engineering team member”)
- Engineer designs reusable *skills* (prompt patterns, tools, guardrails, evals).
- Agents can take on higher-level work: architecture drafts, infra, test harnesses, product/UI support—under governance.
- Mental model: **Engineer becomes agent architect + quality gatekeeper.**

**Role shift across levels:**  
**Coder → Reviewer/Director → Agent Architect & Governance Lead**
