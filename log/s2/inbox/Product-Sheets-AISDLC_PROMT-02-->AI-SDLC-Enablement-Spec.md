ChatGPT Folder > AI SDLC Course Productization > AI-SDLC-Enablement-Spec.md

# AI SDLC Enablement: Product Spec + Curriculum Architecture (10 weeks)

## 1) Decisions (one screen)

- **Tier model (3 tiers) + gating prerequisites**
  - **Tier 1: Foundations (Courseware)** → prerequisite for all
  - **Tier 2: Practitioner (Guided Cohort Enablement)** → requires Foundations completion (or test-out)
  - **Tier 3: Enterprise Accelerator (Transformation Sprint)** → requires Practitioner completion
  - Rationale: matches proven “basic → hybrid → premium coaching” packaging with shrinking cohorts + explicit gating.

- **Pricing model**
  - **Units:** Foundations = **per seat**; Practitioner = **per cohort seat**; Accelerator = **team pack** (or per participant)
  - **List pricing (signals):**
    - Foundations: **$300–$500/seat** (10 weeks)
    - Practitioner: **$2,000–$3,000/participant** (10 weeks, cohort 20–25)
    - Accelerator: **$30k–$50k team pack** (4–6) or **$8k–$15k/participant**
  - **Minimums (practical):** Foundations min **50 seats**; Practitioner min **15 seats** (cap 25); Accelerator min **4-person pack** (cap 6)
  - **Enterprise option:** “**Enablement Pack**” = 100 Foundations + 25 Practitioner + 6 Accelerator (priced as a single order form; volume discounts)
  - **Access duration:** Foundations 6 months content access; Practitioner 12 months; Accelerator 12 months (plus reusable templates)
  - **Support window:** Foundations async support during cohort + 2 weeks; Practitioner +4 weeks; Accelerator +8 weeks

- **Naming scheme**
  - Tiers: **Foundations / Practitioner / Enterprise Accelerator**
  - Replace “Training vs Coaching” with: **Courseware** (scales) vs **Enablement** (guided support / transformation)

- **Gross margin target + operational rationale**
  - Target **60% blended**, with **≥50% floor** on Accelerator by strictly limiting coach hours per participant and pushing everything possible into reusable assets + automated assessment.
  - Constraints assumed real: **no external SaaS, no code upload, approved models only, PHI/PII sensitivities, coaches operate off-network**.

---

## 2) Product spec (tables)

### 2.1 One-page product brief

| Field | Spec |
|---|---|
| Product | **AI SDLC Enablement**: enterprise-safe, code-centric training + enablement to measurably improve delivery speed and quality |
| Primary ICP | Software engineers (brownfield acceleration); secondary: infra/data engineers (workflow + scripting + DevOps) |
| Outcomes | Improve **cycle time, PR throughput, test coverage, docs completeness, adoption, dev satisfaction** |
| Delivery | 10-week program; hybrid live + hands-on labs; evolves into self-paced assets captured from live runs |
| Differentiators | Enterprise-grade constraints + “safe sandbox → brownfield” progression + off-network coaching model |
| Core promise | Teams ship **safer PRs faster** with measurable improvements without violating security controls |
| Tooling stance | Default: **Claude Code CLI**; Week-1 fallback if approvals lag |

### 2.2 Tier comparison (pricing/packaging)

| Tier | Included | Excluded | Seat model | Coaching model | Support channels | Access duration | Prereqs |
|---|---|---|---|---|---|---|---|
| **Foundations (Courseware)** | Recorded lessons, worksheets, labs, starter repo, knowledge checks, prompt-pattern library template, safety drills | Live coaching, brownfield code reviews, exec readouts | Per seat; volume packs | None (optional quarterly webinar add-on) | Knowledge base + async Q&A (ticket/forum) | 6 months | None |
| **Practitioner (Guided Cohort Enablement)** | Foundations + weekly live demo/Q&A + 2hr/wk office hours + milestone reviews + graded lab submissions + cohort forum | Private 1:1 coaching, bespoke implementation on production systems | Per cohort seat (15–25) | Group coaching; “review not do” | Cohort forum + office hours + limited async | 12 months | Foundations or test-out |
| **Enterprise Accelerator (Transformation Sprint)** | Practitioner + 4hr/wk private sessions + implementation reviews + executive KPI readouts + tailored brownfield plan + capstone delivery | “Staff augmentation” coding on client network; broad platform rebuild | Team pack (4–6) or per participant | Small-cohort coaching + governance cadence | Private sessions + exec reviews + async | 12 months | Practitioner (required) |

### 2.3 Operational load model (what scales vs live time)

Assumptions: target cohort sizes of **100–200 (Foundations)** / **20–25 (Practitioner)** / **3–5 (Accelerator)**.

| Activity | Scales? | Foundations (per 100 seats / 10 wks) | Practitioner (per cohort / 10 wks) | Accelerator (per team / 10 wks) |
|---|---:|---:|---:|---:|
| Core content delivery (videos/notes) | Yes | 0 live hrs (recorded) | 0 live hrs (reuse) | 0 live hrs (reuse) |
| Weekly live demo/Q&A | Partly | 1 hr/wk webinar (optional) | 1 hr/wk | 1 hr/wk (focused) |
| Office hours | No | 0 | 2 hr/wk | Included in private sessions |
| Private coaching / implementation review | No | 0 | 0 | 4 hr/wk |
| Grading / rubric feedback | Partly | Auto-checks + 0.5 hr/wk sampling | 2 hr/wk | 2 hr/wk (capstone + PR review) |
| Async support (forum/tickets) | Partly | 1 hr/wk moderation | 1 hr/wk | 1 hr/wk |
| Executive readouts / KPI review | No | 0 | Optional final summary | 1 hr/wk cadence + final deck |
| **Total coach live time** |  | **~10–20 hrs/10 wks** | **~60–70 hrs/10 wks** | **~80–100 hrs/10 wks** |

Margin implication: keep Practitioner to ~6–7 hrs/wk and Accelerator to ~8–10 hrs/wk per team, consistent with the need to prevent coach overload.

### 2.4 Client responsibilities

| Area | Client responsibility | Why it matters |
|---|---|---|
| Repos & environments | Provide access to at least one “training repo” (sanitized is fine) and a target brownfield repo for analysis; provision a safe sandbox if production access is restricted | Enables “safe sandbox → brownfield” progression |
| Tool approvals | Approve model(s), IDE/CLI tooling, and any internal gateways by end of Week 1; define escalation path with security/IT | Prevents early stall |
| Security constraints | Confirm “no external SaaS/no code upload” boundaries; provide redaction guidance and approved prompt policy | Avoids PHI/PII violations |
| Champions | Assign 1 engineering champion + 1 security liaison + 1 exec sponsor | Keeps adoption + approvals moving |
| Time allocation | Protect participant time: 5–7 hrs/wk (Practitioner), 8–10 hrs/wk (Accelerator) | Without time, outcomes don’t move |
| Metrics | Provide baseline measures (cycle time, PR throughput, coverage) and agree on KPI targets | Makes ROI defensible |

---

## 3) 10-week curriculum architecture

### 3.1 Core curriculum map

| Week | Theme | Learning objectives | Live demo(s) | Hands-on lab | Artifact produced | Assessment |
|---:|---|---|---|---|---|---|
| 1 | Enterprise-safe AI workflow kickoff | Safety boundaries, prompt hygiene, repo-less workflow, toolchain plan; establish baseline metrics | “AI SDLC loop” demo; prompt patterns | Offline/safe repo lab: prompt-pattern drills + spec slicing | Prompt-pattern library v0 + personal workflow checklist | Knowledge check + prompt rubric |
| 2 | CLI-driven delivery flow | Use Claude Code CLI (or fallback) for task planning, diffs, PR narration | “ticket → plan → diff” | Implement 1 small feature in sandbox repo | “Safe PR” template + PR description generator | PR rubric score |
| 3 | Testing acceleration | Generate unit tests safely; coverage improvement strategy | Test generation + mutation/edge-case thinking | Add tests to existing module; measure coverage delta | Test plan + coverage delta report | Test rubric + coverage gate |
| 4 | Documentation + architecture extraction | Create ADRs, diagrams, and docs from code without leaking sensitive data | “docs from code” workflow | Generate ADR + C4-style doc set (from sandbox) | ADR + architecture README | Doc rubric |
| 5 | Brownfield analysis mechanics | Dependency mapping, change risk, boundary identification | Large codebase map (demo) | Run brownfield worksheet on target repo (read-only) | Brownfield analysis worksheet + risk-ranked backlog | Worksheet rubric |
| 6 | “Safe PR” strategy for brownfield | Smallest safe changes, scaffolding modules, non-invasive improvements | “scaffold-only PR” demo | Build an observability/test harness sidecar module | PR + rollout plan | PR rubric + peer review |
| 7 | CI/CD + quality gates | Add automation without rewriting pipelines | “quality gates” demo | Add lint/test/coverage gates to pipeline template | Pipeline-as-code template | Gate pass/fail |
| 8 | Observability module build | Logging/tracing/metrics patterns (language variants) | Instrumentation demo | Implement observability module + dashboards stub | Observability module + runbook | Runbook rubric |
| 9 | Security & compliance drills | Redaction, data handling, model choice justification | “prompt redaction review” | Run a red-team prompt drill + remediation | Prompt policy + redaction checklist | Policy rubric |
| 10 | Capstone ship + ROI readout | Ship measurable improvement; present before/after | Capstone walkthrough | Finalize capstone + exec readout deck | Capstone PR(s) + KPI delta report | Capstone rubric + KPI delta |

### 3.2 Two on-ramps (delta-only)

**A) Greenfield track**
- Weeks 2–4 labs focus on building a small module end-to-end (API + tests + docs)
- Weeks 6–8 emphasize “production-like” CI gates and observability in the starter repo
- Capstone: ship a complete feature with tests + docs + pipeline gates

**B) Brownfield track**
- Week 4–5: architecture extraction from real repo (read-only) + dependency graph + risk-ranked backlog
- Week 6: “safe PR” = scaffolding-only (no business logic changes) + non-invasive improvements (tests, docs, observability)
- Capstone: ship 1–3 safe PRs + measurable KPI improvement + documented next backlog

### 3.3 Ensemble vs Cigna deltas (delta-only)
- **Ensemble (SWE, higher baseline):** faster move to brownfield + deeper testing/architecture modules
- **Cigna (infra/data, lower baseline):** Week 1–2 includes extra Git/CLI fundamentals, scripting workflows, and “safe automation” patterns

### 3.4 Week 1 “tooling not ready” plan (off-network, low-permission)
- Week 1 must work without installing full CLI tooling.
- Week-1 fallback path:
  1) Use the safe sandbox starter repo (no sensitive code)
  2) Run prompt-pattern drills + spec slicing + PR narration exercises offline
  3) Establish baseline KPI capture methodology + manual measurement template
  4) If CLI is unavailable: use “diff review” and “test plan generation” exercises that don’t require repo write access
  5) Contingency: shift Week 2 CLI mechanics to Week 3; keep Week 2 on tests/docs that can be done with minimal tooling

### 3.5 Capstone plan (what they ship by week 10)
- **Foundations:** completed labs + prompt library + “safe workflow” playbook
- **Practitioner:** 1–2 PRs in sandbox + brownfield analysis pack + 1 “safe PR” strategy applied to a real repo
- **Accelerator:** 1–3 production-ready PRs (scaffold/observability/tests/docs/pipeline gates) + exec KPI readout + next-quarter backlog

---

## 4) Exercise bank + starter repo plan

### 4.1 Exercise bank

**Foundations (tooling, prompting, workflow)**
- Prompt patterns: intent → constraints → examples → acceptance criteria
- “Ticket decomposition”: convert vague request into 5–10 atomic tasks
- PR narration generator: “what changed / why / risk / how tested”
- Workflow drills: “plan → diff → review” with strict data redaction rules

**Brownfield analysis / documentation / testing**
- Dependency + boundary mapping worksheet run (read-only)
- “Docs from code” pack: ADRs, architecture README, API inventory, runbooks
- Test coverage uplift on a high-risk module (non-invasive)
- Safe refactor proposal: identify refactor candidates and propose PR sequence

**Greenfield module build (observability, test harness, CI improvements)**
- Observability module: structured logs + correlation IDs + basic metrics stubs
- Test harness: contract tests + golden tests + integration tests (starter)
- CI gates: lint/test/coverage thresholds; PR checks; release notes automation

**Safety/compliance drills (redaction, model choice, data handling)**
- Prompt redaction drill: detect and remove PHI/PII from prompts and outputs
- Model-choice justification exercise: “why this model is approved for this data class”
- “Prompt review” workflow: peer-review prompt diffs like code diffs
- Incident drill: “AI suggested unsafe change” → rollback + lesson learned

### 4.2 Safe sandbox starter repo plan (language variants: .NET, Java, Python)

**Repo structure outline (same across languages)**
- `/docs` (ADR templates, architecture README, runbooks, prompt library)
- `/src` (service code; intentionally includes a few “brownfield-like” smells)
- `/tests` (unit + integration skeletons)
- `/infra` (local-only compose + pipeline templates; no external SaaS dependencies)
- `/observability` (logging/tracing/metrics wrappers)
- `/scripts` (CLI helpers: lint/test/coverage/docgen)
- `/tickets` (sample user stories + acceptance criteria)

**Sample tickets / user stories**
- “Add correlation ID propagation end-to-end”
- “Increase unit test coverage on parser module by +20%”
- “Generate ADR for chosen architecture approach + trade-offs”
- “Add CI quality gate: fail build if coverage drops”
- “Create runbook: local dev setup + troubleshooting”
- “Introduce safe input validation + error taxonomy (no behavior change)”

**Evaluation rubric hooks (per ticket)**
- Correctness (meets acceptance criteria)
- Test quality (edge cases, readability, flakiness avoidance)
- Documentation quality (ADR clarity, runbook completeness)
- Safety/compliance (no sensitive data, prompt hygiene, model boundary adherence)
- Delivery hygiene (small PRs, clear narration, risk assessment)

---

## 5) Content capture + productization pipeline

### 5.1 Repeatable system (turn live delivery into product assets)
- Record every live demo, weekly Q&A, and capstone review.
- Capture artifacts: lab handouts, solutions, PR exemplars, “good/bad” prompt examples, rubric-scored submissions.
- Normalize: convert to a consistent “lesson + lab + rubric” package; remove proprietary content; tag by week/theme.
- Version: Courseware versions (e.g., **v0.1** MVP, **v0.2** after 2 cohorts); per-week module versions.
- Edit cadence: weekly “ship room” (publish updated assets each Friday); monthly consolidation release.

### 5.2 Templates (copy/paste sections)

**Lesson plan template**
- Title:
- Audience level:
- Timebox:
- Objective:
- Prereqs:
- Demo steps (scripted):
- Key takeaways:
- Common failure modes:
- References (internal only):

**Lab template**
- Title:
- Scenario:
- Starting state:
- Constraints (security/data/tooling):
- Tasks:
- Acceptance criteria:
- Submission format:
- Stretch goals:
- Rubric mapping:

**Rubric template**
- Dimension:
- 0 / 1 / 2 / 3 / 4 scoring anchors:
- Evidence required:
- Auto-checks (if any):
- Reviewer comments:

**Brownfield codebase analysis worksheet**
- Repo context (language, services, deployment model):
- Top-level dependency map:
- Data boundaries + sensitive zones:
- Change-risk heatmap:
- Top 10 “safe PR” candidates:
- Test coverage baseline + opportunities:
- Observability gaps:
- Suggested 4-week PR sequence:

**Prompt-pattern library template**
- Pattern name:
- When to use:
- Inputs required:
- Prompt structure:
- Output contract:
- Safety notes (redaction, data class):
- Example (sanitized):
- Variants:

### 5.3 10-week internal execution plan (so we don’t fall behind)
- Week 1: finalize starter repo + rubrics + prompt library v0; record kickoff
- Week 2: publish “ticket → plan → diff → PR narration” module; capture top PR exemplars
- Week 3: publish testing module + coverage gates; create auto-check harness
- Week 4: publish docs/ADR/architecture module + doc rubric
- Week 5: publish brownfield worksheet + sample completed worksheet
- Week 6: publish safe PR playbook + scaffolding patterns
- Week 7: publish CI/CD gates templates (ADO-oriented) + language variants
- Week 8: publish observability module variants + runbooks
- Week 9: publish compliance drill pack + prompt review workflow
- Week 10: publish capstone rubric + exec readout deck template + KPI reporting template

---

## 6) GTM basics (tight, enterprise-focused)

### 6.1 ICP positioning (Ensemble SWE vs Cigna infra/data)
- **Ensemble SWE:** brownfield acceleration + safer PRs faster; advanced testing/docs/architecture extraction.
- **Cigna infra/data:** workflow + scripting automation + safe AI usage; extra fundamentals and guardrails.

### 6.2 Buyer roles + buying triggers
- Buyers: VP Eng, Director Eng, Platform/DevEx lead, Security/Compliance partner, L&D leader.
- Triggers:
  - GenAI rollouts stalled by security/tool approvals
  - Delivery performance plateau; need cycle time reduction
  - Quality issues: escaped defects / low coverage
  - Exec mandate to “use AI” but no safe operating model

### 6.3 Benchmarks used (pricing sanity check)
- Self-paced enterprise learning platforms: often **$200–$600/user/year** or **$14–$30/user/month**.
- Instructor-led workshops: often **$500–$1,500/participant**.
- Cohort programs: often **$2,000–$7,000/participant**.
- Enterprise packages: typically custom and higher.

### 6.4 Sales narrative + objection handling

**Narrative**
- Install a repeatable AI SDLC operating model under enterprise constraints: teams ship smaller, safer PRs with measurable improvements in cycle time, coverage, and documentation—without leaking code or violating PHI/PII policies.

**Common objections**
- “Security will never allow it.” → Designed for approved models + internal execution + prompt hygiene + redaction drills + prompt review workflow.
- “We don’t have time.” → Foundations is low-touch; Practitioner is 5–7 hrs/wk; Accelerator is limited seats with direct KPI focus.
- “This will turn into consulting hours.” → Clear tier boundaries + fixed coaching caps + coach off-network stance.
- “How do we prove ROI?” → Baseline + mid + end KPI deltas across DORA/SPACE-aligned metrics.

### 6.5 FAQ (product + security + tooling constraints)
1) Do you require access to our code? **No.** Brownfield work is performed by participants; coaches operate off-network.  
2) Do you upload code to external tools? **No.**  
3) What if tooling approvals slip? Week-1 runs on low-permission exercises; schedule resequences without blocking.  
4) What do participants ship? Safe PRs, tests, docs, and a capstone with KPI deltas (tier-dependent).  
5) What languages are supported? .NET, Java, Python starter repo variants (same structure).  
6) What’s the cohort size? Foundations 100–200, Practitioner 20–25, Accelerator 3–5 (or 4–6 pack).  
7) What metrics do you track? Cycle time, PR throughput, coverage, docs completeness, adoption rate, satisfaction.  
8) Is this “Copilot training”? No. It’s an SDLC workflow + governance model for enterprise constraints.  
9) Do you provide certification? In v2.  
10) What’s required from leadership? Exec sponsor + time protection + approval acceleration.

### 6.6 Risk register + mitigations (product-grade)

| Risk | What happens | Mitigation |
|---|---|---|
| Security/data handling | Leakage risk | Sandbox-first, approved models only, redaction + prompt reviews |
| Tool access & approvals | Week 1–2 stalls | Offline Week-1 plan; shift sequencing; security liaison escalation |
| Adoption/engagement | Dropout in self-paced | Weekly milestones, dashboards, manager comms |
| Executive buy-in | No sustained change | Exec sponsor + KPI reporting + alignment to business outcomes |
| Delivery capacity | Coach overload | Hard caps: 25 in Practitioner; ≤6 in Accelerator pack |
| IP/productization | Can’t reuse content | SOW addendum clarifies anonymized reuse rights |

---

## 7) SOW addendum draft (concise)

### 7.1 Inclusions/exclusions per tier

**Foundations**
- Includes: access to courseware, labs, starter repo, knowledge checks, prompt library templates.
- Excludes: live coaching, private sessions, custom implementation.

**Practitioner**
- Includes: Foundations + weekly live session + office hours + graded submissions + cohort forum.
- Excludes: private 1:1 coaching, delivery of custom code changes inside client network.

**Enterprise Accelerator**
- Includes: Practitioner + private sessions + tailored brownfield plan + exec KPI readouts + capstone delivery support.
- Excludes: staff augmentation; on-network engineering work unless explicitly contracted.

### 7.2 Assumptions/dependencies
- Tool approvals and approved model access targeted by end of Week 1; delays may require schedule resequencing.
- Participants have baseline skills appropriate to tier; Practitioner/Accelerator assume Git and testing familiarity.
- Client provides sponsor + champion + security liaison.

### 7.3 Success criteria/KPIs
Baseline + end-of-program delta targets across:
- cycle time / lead time, PR throughput, test coverage, docs completeness, adoption rate, developer satisfaction.
Deliverables include a final KPI delta report and capstone rubric scoring.

---

## 8) Two variants

### 8.1 MVP deliverable (within 10 weeks)
- One live 10-week cohort (Practitioner-style) recorded end-to-end.
- Starter repo v0 + 10 labs + rubrics (PR/tests/docs/prompts).
- Brownfield worksheet + safe PR playbook.
- KPI baseline + end report template.
- Minimal secure portal structure to distribute assets.

### 8.2 v2 scaled product (within 6 months)
- Full self-paced Foundations library (edited videos + transcripts + auto-graded checks).
- Practitioner cohorts run by trained coaches (standardized playbooks).
- Optional certification: capstone + rubric threshold + timed knowledge check.
- Train-the-trainer kit + facilitator guide + grading calibration.
- Automated KPI ingestion where possible + executive dashboards.

---

## 9) Assumptions + open questions + decision points

### 9.1 Assumptions made
- Approved model path for CLI-driven workflows is available within 2 weeks.
- Clients will allow a sandbox repo that is non-sensitive for early labs.
- Practitioner cohorts hold at 20–25; Accelerator limited to ≤6 per pack.
- KPI baselines are measurable (even if manually at first).

### 9.2 10 highest-leverage questions to validate next
1) What model(s) are approved today (and what data classes are allowed)?  
2) Can participants run CLI tools locally, or must everything be inside a locked VM?  
3) What’s the fastest path to a safe sandbox repo in each client environment?  
4) Which KPIs can be measured automatically vs manually right now?  
5) What is the acceptable “coach interaction surface” (Zoom only? internal chat?)  
6) Who owns tool approval decisions (names/roles)?  
7) What is the minimum acceptable capstone impact (e.g., coverage +10%, cycle time −X%)?  
8) Do you want an internal certification badge, or an external credential later?  
9) What’s the target purchase motion: L&D budget, engineering budget, or transformation initiative?  
10) What IP reuse language will each client accept for productization?

### 9.3 Decision points + if/then paths
- **If tool approvals slip past Week 2:** run Weeks 1–4 fully on sandbox + read-only brownfield analysis; move “write PRs on real repo” to Weeks 7–10.
- **If security forbids any repo access in training:** pivot to “pattern transfer” model—participants apply patterns asynchronously; capstone becomes docs/tests/observability scaffolding only.
- **If Practitioner demand exceeds capacity:** add cohorts, not seats; enforce 25 cap; use standardized rubrics and recorded demos.
- **If Cigna baseline is too low for Practitioner pacing:** require a short “Foundations Bridge” (Git + CLI + prompt basics) before Week 1.

---

## Source notes (moved out of the main body)

All references below point to your attached **Research_Packet.md** (line numbers from that file).

- **Security and enterprise constraints** (internal execution, approved models, sensitive data concerns): lines **15–18** and **117–123**.
- **Tier names + pricing signals** (Foundations / Professional/Practitioner / Enterprise Accelerator, plus pricing ranges): lines **22–28**.
- **Tiered packaging patterns + prerequisite gating**: lines **64–72**.
- **Outcome metrics framing (DORA + SPACE; cycle time and related measures)**: line **20** and lines **90–101**.
- **Content capture pipeline for productization**: lines **115–116**.
- **Coach capacity risk + need for caps**: lines **125–126**.
- **IP reuse / anonymization in productization + SOW addendum outline**: lines **127–136**.
