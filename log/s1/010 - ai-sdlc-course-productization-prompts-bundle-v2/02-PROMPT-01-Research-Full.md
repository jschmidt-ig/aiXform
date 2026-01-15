ChatGPT Folder > AI SDLC Course Productization Prompts (Research + Thinking) > 02-PROMPT-01-Research-Full.md

You are a research analyst specializing in:
(1) enterprise technical training businesses,
(2) AI-assisted software delivery (AI SDLC),
(3) B2B pricing/packaging and enablement programs.

You MUST use web research and include citations for factual claims and examples.

GOAL
Create a “Research Packet” to inform product packaging, tier naming, delivery model, and pricing for an AI SDLC course product we are productizing from consulting delivery.

CONTEXT + CONSTRAINTS (do not ignore)
- Use the embedded source material below (problem, constraints, requirements).
- Treat enterprise security constraints as real: no external SaaS, no code upload, approved models only, security/red-team review processes, PHI/PII sensitivities.
- Coaching should ideally not require coaches to have client laptops or internal network access (“off network” support).

DELIVERABLES (must produce all; structure exactly)

1) Executive summary (<=10 bullets): key findings + implications for our offer

2) Market map (8–15 comparables, cited)
   - Table: Company | Offer type | Delivery model | Pricing signals (if public) | Tiering/packaging patterns | Notes | Sources
   - Prefer primary sources (company pages/pricing pages) and reputable outlets

3) Pricing benchmarks (cited)
   - Typical ranges and common units (per-seat, cohort, team pack, enterprise)
   - What costs more and why (coaching, private cohort, certification, custom labs, duration)
   - If pricing is not public, say so and cite your inference sources

4) Packaging patterns (what works in the market, cited)
   - Common tier structures (materials vs office hours vs embedded coaching)
   - Prerequisites/gating patterns (foundations before advanced coaching)

5) Naming patterns (replace “belt” terminology)
   - 12–20 naming options grouped by tone (enterprise, technical, playful)
   - Pros/cons and what the market tends to do

6) Measurement / KPI menu
   - Propose 8–12 measurable outcomes
   - Label each as (Controllable) vs (Lagging/Org-dependent)
   - Include at least: cycle time proxies, PR throughput, defect/quality proxies, docs completeness, test coverage, dev satisfaction, adoption

7) Recommendations (evidence-driven)
   - 2–3 packaging models that fit the constraints, with rationale
   - Suggested pricing structure(s), including team packs, and why
   - Suggested gross margin targets + typical ranges (cite if possible)

8) Risk register + mitigations (table)
   - Include: security, adoption, tool access, exec buy-in, delivery capacity, data handling

9) Draft SOW addendum outline (concise)
   - Inclusions/exclusions per tier
   - Client responsibilities
   - Assumptions/dependencies
   - Success criteria/KPIs

10) ATTACHMENT: Research_Packet.md
   - Create a clean, self-contained markdown “packet” suitable for attachment in Run 2.
   - Requirements:
     - 1–2 pages max (tight)
     - MUST include: recommended packaging + naming + pricing ranges + key tables + constraints summary
     - MUST include citations in-line where applicable
   - Output format requirements for this attachment:
     - Put the entire attachment content inside ONE markdown code block.
     - Start the attachment with the line: `# Research_Packet`
     - End the attachment with the line: `# End_Research_Packet`
     - Do not include anything else inside the code block.

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
