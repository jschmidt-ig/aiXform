# Proposal: AI Accelerated Software Development (10-Week Pilot)

**Prepared for:** DevDatta Halbe (SVP, Product Engineering)  
**Prepared by:** Praxis  
**Date:** 2026-01-20

---

## 1) Executive summary

This proposal describes a 10-week pilot to enable **AI-accelerated software delivery** for 1-3 development teams. The focus is practical: ship more reliably using agentic coding workflows (plan -> diff -> test -> narrate), under enterprise security constraints, with measurable outcomes.

The pilot is structured as three phases:

1. **Fundamentals (Weeks 1-2):** mental model + safety gate (recordable courseware)
2. **Labs (Weeks 3-6):** hands-on labs producing concrete artifacts (PRs, tests, docs, runbooks)
3. **Applied (Weeks 7-10):** coached implementation on real Ensemble work + executive readout

---

## 2) Why this matters (in plain terms)

Ensemble’s AI goals depend on the organization’s ability to **ship software faster and safer**:
- agents need tools
- tools require software
- software velocity becomes a multiplier across all AI initiatives

This pilot targets the near-term highest ROI: **AI-assisted/agentic SDLC**.

---

## 3) Pilot goals and measurable outcomes

### Goals by Week 10
- A repeatable, safe workflow for AI-assisted development (tooling + rules + review discipline)
- Teams consistently using an agentic coding method for delivery work
- At least one high-signal improvement per team (capstone PRs) backed by metrics

### Target measurable outcomes
- Delivery: PR throughput, time-to-merge, cycle time (ticket -> merge)
- Quality: test/coverage deltas on high-risk areas, reduced review thrash
- Enablement: adoption rate (self-report + signals where available), developer satisfaction

---

## 4) Scope and delivery model (10 weeks)

### Cohort sizing
- 1-3 cohorts
- Up to 20 participants per cohort
- Recommended first run: ~15 participants (cap ~20)

### Weekly cadence (typical)
- 1 module block (~1 hour)
- 2 labs/workshops (~2 hours each)
- 1 review/Q&A block (~1 hour)
- short submission/retro (~1 hour)

Total structured time: **~6 hours/week**, with Applied work overlapping normal delivery.

### Week-by-week (high level)
- **Week 1:** fundamentals + safe use kickoff, baseline metrics, enablement discovery
- **Week 2:** agentic coding foundations, first sandbox PR
- **Week 3:** lab sprint 1: feature delivery + PR narration workflow
- **Week 4:** lab sprint 2: testing acceleration + coverage delta reporting
- **Week 5:** lab sprint 3: docs + architecture extraction (ADR/runbook)
- **Week 6:** workflow integration into existing SDLC (branching, PR rules, review norms)
- **Week 7:** coached delivery on real work (safe PR selection + execution)
- **Week 8:** expand to higher-impact tickets + quality gates
- **Week 9:** hardening + mid/end metrics capture + rollout guidance drafting
- **Week 10:** capstone + executive readout + next 90-day plan

---

## 5) Deliverables (what Ensemble gets)

### During Labs (Weeks 3-6)
- PR narration templates (what/why/risk/how-tested)
- Architecture README + ADR v1 + dependency/boundary notes
- Risk-ranked backlog of “safe PR” candidates
- Test plan + coverage/test delta report
- Observability + security drill artifacts (logging schema, correlation IDs, redaction checklist)

### During Applied (Weeks 7-10)
- Capstone PR package: 1-3 meaningful PRs per team
- Team AI SDLC playbook v1 (how we work, prompts, permissions, review gates)
- Executive readout: KPI deltas + rollout recommendations + next 90-day plan

---

## 6) Enablement and security assumptions

### Tooling
- Primary agentic harness: **Claude Code CLI**

### Environment options (choose early)
- **Isolated cloud lab environment** (recommended)
- Dev containers on developer machines
- Windows + WSL-based setup

### Safety rules (non-negotiable)
- No PHI/PII or sensitive code/data in prompts unless explicitly approved and governed
- Least-privilege tool permissions (read-only first where appropriate)
- Human review required for merges and any production-affecting changes
- Prompt injection awareness: untrusted inputs are isolated and labeled

---

## 7) Roles and responsibilities

### Praxis
- Deliver instruction, labs, and coaching
- Provide templates, rubrics, and workflow playbooks
- Support enablement decisions (policy + environment patterns)
- Run measurement and produce executive readout

### Ensemble
- Identify 1-3 target teams and participant list
- Provide time protection for participants (8-10 hrs/week)
- Provide access to tooling and a safe lab environment
- Provide KPI sources where available (ADO, dashboards) or agree to manual sampling

---

## 8) Measurement plan (simple and defensible)

- **Week 1:** baseline capture
- **Week 6:** mid-point directional check
- **Week 10:** final results + narrative

KPI set (initial):
- cycle time (ticket -> merge)
- PR throughput and PR size
- review iteration count / reopen rate
- targeted test/coverage delta
- adoption rate + short satisfaction survey

---

## 9) Commercials: hourly pilot + list pricing transparency

### Hourly pilot (recommended for first run)
Ensemble already has an approved contract vehicle for hourly billing. For the first run, Praxis proposes we deliver under that contract to minimize procurement friction.

**Estimated instructor effort (first pilot):** ~150-210 hours total  
**Pilot cost:** `hourly_rate × (150-210)`

This approach is intentionally simple: bill only actual time spent.

### List pricing (for future rollouts)
Forward pricing model for steady-state delivery:
- Fundamentals: **$500/seat**
- Labs: **$2,500/seat**
- Applied: **$20,000 per cohort**

Program total formula (C cohorts, N seats per cohort):
- `C × ( $3,000 × N + $20,000 )`

Examples:
- 1 cohort × 15 seats: $65,000
- 1 cohort × 20 seats: $80,000
- 3 cohorts × 15 seats: $195,000
- 3 cohorts × 20 seats: $240,000

---

## 10) Decisions needed to start (end of Week 1)

1. Cohort selection (1-3 teams) and participant list
2. Environment choice (cloud lab vs dev containers vs WSL)
3. Tool access path (Claude Code CLI usage + logging policy)
4. Data handling rules (what can/can’t enter prompts; redaction expectations)
5. KPI access approach (ADO + dashboards vs manual sampling)

---

## 11) Next steps

1. Confirm pilot start date and cohort count (1-3)
2. Lock environment choice + access plan
3. Schedule Week 1 baseline + enablement kickoff
4. Publish participant calendar blocks for predictable cadence
