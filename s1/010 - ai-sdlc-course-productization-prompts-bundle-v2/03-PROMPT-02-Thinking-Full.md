ChatGPT Folder > AI SDLC Course Productization Prompts (Research + Thinking) > 03-PROMPT-02-Thinking-Full.md

You are a product strategist + curriculum architect for AI SDLC enablement.
Do NOT browse the web. Use only the embedded source material and the attached Research_Packet.md file.

INPUTS YOU HAVE
1) Embedded source material (problem, constraints, requirements) — below.
2) An attached file named `Research_Packet.md` produced by the research run.
   - If the attachment is missing, stop and ask for it.

TASK
Synthesize the final product and course design and produce the full “product-grade” deliverable set.
Be decisive: pick a path when trade-offs exist, and justify briefly.

OUTPUT (structure exactly)

1) Decisions (one screen)
   - Tier model (3 tiers) and gating prerequisites
   - Pricing model: units (seat/team/cohort), minimums, enterprise option, access duration, support window
   - Naming scheme: tier names + replacement for “Training vs Coaching” (more professional)
   - Gross margin target + operational rationale

2) Product spec (tables)
   - Tier comparison table: Included/Excluded, seat model, coaching model, support channels, access duration, prerequisites
   - Operational load model: what requires live time vs what scales (include assumptions)
   - Client responsibilities table (repos, approvals, champions, time allocation, security constraints)

3) 10-week curriculum architecture
   - Core curriculum map table:
     Week | Theme | Learning objectives | Live demo(s) | Hands-on lab | Artifact produced | Assessment
   - Two on-ramps (delta-only):
     A) Greenfield track
     B) Brownfield track (large codebase analysis, docs generation, testing, “safe PR” strategy)
   - Ensemble vs Cigna deltas (delta-only)
   - Week 1 “tooling not ready” plan: off-network, low-permission exercises + contingency path
   - Capstone plan (what they ship by week 10)

4) Exercise bank + starter repo plan
   - Exercise bank grouped by:
     - Foundations (tooling, prompting, workflow)
     - Brownfield analysis/documentation/testing
     - Greenfield module build (observability module, test harness, CI improvements)
     - Safety/compliance drills (redaction, model choice, data handling)
   - “Safe sandbox starter repo” plan with language variants (.NET, Java, Python):
     - repo structure outline
     - sample tickets/user stories
     - evaluation rubric hooks

5) Content capture + productization pipeline
   - Repeatable system to convert live delivery into product assets:
     - what to record, templates, versioning, editing, release cadence
   - Templates (provide as copy/paste sections):
     - lesson plan template
     - lab template
     - rubric template (PRs/tests/docs/prompts)
     - “brownfield codebase analysis” worksheet
     - prompt-pattern library template
   - 10-week internal execution plan (what to build each week so we don’t fall behind)

6) GTM basics (tight, enterprise-focused)
   - ICP positioning (Ensemble SWE vs Cigna infra/data)
   - Buyer roles + buying triggers
   - Sales narrative + objection handling
   - FAQ (product + security + tooling constraints)

7) SOW addendum draft (concise)
   - Inclusions/exclusions per tier
   - Assumptions/dependencies
   - Success criteria/KPIs

8) Two variants
   - MVP deliverable within 10 weeks
   - v2 scaled product within 6 months (asynchronous/self-paced, certification option, partner enablement)

9) Assumptions + open questions + decision points
   - Assumptions you made
   - 10 highest-leverage questions to validate next
   - Decision points and “if/then” paths (tool approvals slip, security constraints, cohort size changes)

CONSTRAINTS
- Practical and delivery-aware: cannot create a perfect course in 10 weeks.
- Optimize for sell-by-seat with optional coaching while preserving quality.
- Preserve high overlap across Ensemble and Cigna.
- Prefer coach “off network” operations; avoid requiring client laptops/internal access.
- Use Claude Code CLI as primary workflow tool; provide week-1 fallback plan due to approvals.

SOURCE MATERIAL (embedded; do not ask me to paste anything)
# Source material (embedded so prompts are standalone)

## Original problem statement
<problem>
Help me create a structured prompt for ChatGPT 5.2 Pro Research to assist with the following problem:

For Integral Brain, we decided on our product strategy to create an AI SDLC course for our client Ensemble and build that into a product that we can sell.

I've got a couple of problems I'm working on simultaneously, and I want you to help me take a structured approach.

What is the opportunity? We got Ensemble to pay us for the next 10 weeks for consulting work. So we're making that consulting work into AI SDLC training for their software engineers. Then we've got another client (Cigna), and they have more infrastructure/data engineers. We want to do an AI course for them. We'd like it to be a lot of overlap. There’s a different approach probably in the beginning, but we’ll work that out. The main target is software engineers. The infrastructure/data engineers are “less technical,” but can write scripts and code.

We want to figure out the products we want to sell as this AI SDLC because the way we’re delivering this isn't really a product model. We’re spending ~40 hours/week with these teams over the next 10 weeks; that’s consulting, not scalable. The product model is a course we can sell more independently of hours worked.

Two problems:
1. Developing the course, strategy, and content for the course
2. Developing the model for product and product delivery

Initial thought: over the next 10 weeks with Ensemble SWEs and Cigna infra/data engineers, we build the course content as we teach it (hands-on). We extract that content and package it to sell as a product where it’s more about the material, supplemented with coaching services.

We’re calling it (placeholder terms):
- “White belt / Green belt / Black belt”
- “Training vs Coaching”

Training = material + seat-based pricing (students consuming materials).
Coaching = working directly with teams (service component; not necessarily billed hourly, but time-based in reality).

Tier mix (placeholder):
- White: 100% training, no coaching
- Green: 50/50 training + coaching (e.g., 1 hour/day materials + 1 hour/day coaching)
- Black: 100% coaching (after completing lower tiers)

Pricing placeholder (per student): $100 / $1,000 / $10,000. Black belt would be fewer people (e.g., 4). Want AI advice and market research on how other companies deliver and price this.

Course content idea:
- 10-week course
- Provide ~1 hour/day of content initially (live demos); later evolve to video/worksheets.
- Also coaching throughout.
- Custom materials based on client needs.
- Need a syllabus and outline.

Differentiation: greenfield vs brownfield projects.
- Brownfield: teach AI analysis on large codebases; generate architecture/product docs; AI-assisted unit tests and coverage; get comfortable with tooling before production code changes.
- Brownfield approach: start with separate support modules (observability stack, test harness, end-to-end tests) to give a “greenfield-like” experience before touching core code.
</problem>

## Captured inputs + constraints
<captured-inputs-and-constraints>
## Audience + outcomes
- Outcomes: want controllable metrics; open to suggestions. Initial thoughts:
  - Delivery velocity / cycle time (idea → code → test → production)
  - Developer experience survey (NPS-like or value rating of course delivery)

- Day 1 differences:
  - Assume repo access + permissions.
  - Tool constraints: may not be able to install Claude Code CLI; may need an internal Claude model setup.
  - Assume by end of week 1 they have tools. Need week-1 content while approvals/setup happen.

- Skill baseline:
  - Ensemble: mid/senior SWEs; varying Copilot exposure; competent in Git; decent testing maturity.
  - Cigna infra/data engineers: less experienced; basic scripting; likely little/no LLM + Git tooling exposure.

## Delivery logistics
- First 10 weeks: synchronous, live lecture/demo + hands-on lab.
- Long term: transition to asynchronous/self-paced; optional office hours.
- Cohort targets:
  - Tier 1 (training-heavy): 100–200 (possibly enterprise-wide)
  - Tier 2 (hybrid): 20–25
  - Tier 3 (coaching-heavy): 3–5
- Duration/cadence: 10 weeks is contract-driven; open to alternative productized formats:
  - 1–2 hours/day model
  - ~6 hours/day bootcamp model
  - wants suggestions based on common market patterns

## Tooling + constraints
- Primary tool: Claude Code CLI.
- Constraints: assume strict enterprise controls:
  - no external SaaS, no code upload, approved models only
  - security/red-team review processes
  - PHI/PII sensitivities
- Coach access constraint:
  - Prefer not needing client laptops or internal network access; want to assist “off network.”

- Stack preferences:
  - Both clients: Azure; repos in Azure DevOps (ADO).
  - Later: make course apply to AWS and be language-independent.
  - Likely need parallel examples: .NET, Java, Python.
  - Ensemble examples: .NET
  - Internal demos: Python

## Product model + pricing
- Placeholder pricing was exploratory; wants market-driven options.
- Pricing unit: one-time training + X weeks support (not annual), flexible.
- Open to team packs.
- Gross margin not defined; wants recommended targets.

## Positioning + naming
- Not in love with “belt” terminology; open to alternatives; wants more professional.
- Tone: professional with personality; not overly corporate; still enterprise-friendly.
</captured-inputs-and-constraints>

## Additional requirements (include all)
<additional-requirements>
Include ALL of the following in your outputs:

A) Make the output product-grade:
- 1-page product brief
- pricing/packaging table
- sales narrative
- FAQ
- draft SOW addendum (deliverables + inclusions/exclusions)
- content capture pipeline (turn live delivery into product assets)

B) Make it operational and repeatable:
- curriculum map (week → lessons → objectives → artifacts → assessment)
- exercise bank split by greenfield vs brownfield
- safe sandbox starter repo plan
- rubrics for PRs, tests, docs, prompts

C) Make it defensible in market:
- competitive/market benchmarks with citations
- risk register + mitigations

D) Force clarity:
- explicit assumptions, open questions, decision points
- two variants: MVP in 10 weeks vs scaled v2 in 6 months
</additional-requirements>
