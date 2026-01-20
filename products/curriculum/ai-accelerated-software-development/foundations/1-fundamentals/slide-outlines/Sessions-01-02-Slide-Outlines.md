# Sessions 01–02 — Slide Outlines (Fundamentals)

## Session 1 — Course orientation

### 1) Session summary
- **Title:** Course orientation: what “AI Accelerated Software Development” means here
- **Purpose (1 sentence):** Align on the mental model, the delivery phases, and the safety bar before we talk about tools.
- **Learning objectives (3):**
  1. Describe the course’s 3-layer model (model, harness, workflow/governance).
  2. Explain what “agentic coding” means operationally (task → plan → artifact).
  3. State the safety gate expectations for Fundamentals (critical safety concepts).
- **If learners only remember 1 thing:** **Tools matter less than workflow + safety constraints.**

### 2) Slide-by-slide outline

#### Slide 1 — Welcome + outcomes
- **Key bullets:**
  - What we’ll cover in Fundamentals (2 weeks)
  - What you’ll be able to do after
  - Lecture-only: no tool execution in this phase
- **Speaker notes:** This course is about building reliable habits and mental models, not memorizing product UIs.
- **Visual:** Simple agenda timeline (Weeks 1–2 Fundamentals, 3–6 Labs, 7–10 Applied).
- **Time:** 2 min

#### Slide 2 — The problem we’re solving
- **Key bullets:**
  - AI can increase throughput *or* increase risk/thrash
  - Enterprise reality: constraints + approvals + auditability
  - Goal: safer, smaller PRs; better test/docs velocity
- **Speaker notes:** “More code faster” is not the target; “more *verified* change faster” is.
- **Visual:** Two-lane diagram: “ad hoc AI use” vs “workflow-driven AI use”.
- **Time:** 2 min

#### Slide 3 — What “agentic coding” means (in plain language)
- **Key bullets:**
  - Not “chatting until it works”
  - A loop: clarify → plan → propose artifacts → verify → narrate
  - Humans stay responsible for decisions
- **Speaker notes:** Agents are just workflow automation around an LLM; they aren’t magic.
- **Visual:** Agentic loop (Plan → Act → Observe → Reflect → Iterate).
- **Time:** 3 min

#### Slide 4 — The 3-layer stack (core mental model)
- **Key bullets:**
  - Layer 1: **Model** (tokens, inference)
  - Layer 2: **Harness** (UI/IDE/CLI; context assembly; tools)
  - Layer 3: **Workflow/Governance** (permissions, approvals, audit)
- **Speaker notes:** Most enterprise wins come from layer 3: guardrails and repeatability.
- **Visual:** 3-layer stack diagram.
- **Time:** 3 min

#### Slide 5 — Course phases (why Fundamentals is lecture-only)
- **Key bullets:**
  - Fundamentals: mental models + safety (no execution)
  - Labs: hands-on tool practice + scaffolding
  - Applied: adapt to real projects + team playbook
- **Speaker notes:** We separate understanding from execution to avoid unsafe early habits.
- **Visual:** Phase table with outcomes per phase.
- **Time:** 2 min

#### Slide 6 — Safety gate (what “hard fail” means)
- **Key bullets:**
  - Critical safety concepts are non-negotiable
  - Prompt injection recognition + response
  - Least privilege tool permissions (approval gates)
- **Speaker notes:** Passing the safety gate is about judgment under ambiguity, not trivia.
- **Visual:** “Pass criteria” box + critical safety badge.
- **Time:** 2 min

#### Slide 7 — How lectures will run (fast pattern)
- **Key bullets:**
  - Concept → diagram → example → misconception → “what to do Monday morning”
  - 1 on-slide “demo moment” per session
  - End with a 30-second recap line
- **Speaker notes:** Expect lots of practical checklists and templates you can reuse.
- **Visual:** Session template strip (Concept / Example / Demo / Risks / Recap).
- **Time:** 2 min

#### Slide 8 — Common misconceptions (callouts)
- **Key bullets:**
  - Misconception: “AI output quality = model quality”
  - Reality: context + contracts + verification dominate
  - Misconception: “More autonomy is always better”
  - Reality: autonomy without guardrails amplifies mistakes
- **Speaker notes:** We’ll keep returning to these; they explain most failures in practice.
- **Visual:** Two callout boxes.
- **Time:** 3 min

#### Slide 9 — What to do next (prep)
- **Key bullets:**
  - Read your org’s acceptable-use policy (if available)
  - Write down 1 real task you want help with in Labs
  - Bring examples of “constraints” you work under
- **Speaker notes:** The fastest way to get value is to map concepts to your own constraints.
- **Visual:** Checklist.
- **Time:** 1–2 min

### 3) Demo-in-lecture plan (no execution required)
- **Demo moment 1 (Slide 3 or 7):** “Task → Plan → Artifact” contract example
  - **Snippet (on-slide):**
    ```text
    TASK: Add request id correlation to service logs.
    PLAN: (1) Identify entry points, (2) Add middleware, (3) Update log schema, (4) Add tests.
    ARTIFACTS: patch diff + test plan + rollout notes + risk checklist.
    ```
  - **What to point out:** Contracts reduce ambiguity; artifacts are reviewable; “plan-first” reduces thrash.
  - **What could go wrong:** Vague tasks lead to wide-scope changes; missing risks leads to unsafe merges.

### 4) Examples bank
- **Good example:** “Propose a minimal change plan for adding correlation IDs, including tests and risk mitigations.”
- **Bad example (why it fails):** “Improve logging across the whole system.” (scope explosion, no constraints, no acceptance criteria)
- **Enterprise-safe example:** Provide a *sanitized* architecture summary + required log fields + allowed output format; explicitly exclude secrets/PHI.

### 5) Graphics pack (image/diagram prompts)
- **Diagram:** 3-layer stack (model → harness → workflow/governance)
  - Prompt: “A clean 3-layer stack diagram labeled Model, Harness, Workflow/Governance; minimal enterprise style; monochrome.”
  - Nano Banana variant: “Create a simple layered diagram: bottom ‘Model’, middle ‘Harness’, top ‘Workflow/Governance’; include small icons (brain, terminal, shield).”
  - Label: flowchart
  - Placement: Slide 4
- **Infographic:** “Ad hoc AI use vs workflow-driven AI use”
  - Prompt: “Two-column comparison infographic: Ad hoc vs Workflow-driven; show risks and outcomes; enterprise minimal design.”
  - Nano Banana variant: “Two-lane infographic with headings ‘Ad hoc’ and ‘Workflow’; bullet icons for risks/outcomes.”
  - Label: infographic
  - Placement: Slide 2

### 6) Safety & risk callouts
- **Relevant risks:** Over-trusting outputs; scope creep; leaking sensitive context.
- **Mitigations to mention:** Use output contracts; keep tasks small; sanitize context; require human review.
- **Critical safety concepts:** (Preview) Least privilege + prompt injection (fully covered later).

---

## Session 2 — Tooling + constraints (enterprise reality)

### 1) Session summary
- **Title:** Enterprise constraints: what you can’t do (and how to still win)
- **Purpose (1 sentence):** Establish safe boundaries for data, tooling, and approvals so AI helps without creating compliance incidents.
- **Learning objectives (3):**
  1. Classify common data types into “safe / redact / never include” for AI contexts.
  2. Explain why “approved models only + no external SaaS” changes workflow design.
  3. Apply a simple rule: **untrusted text cannot directly drive tool actions**.
- **If learners only remember 1 thing:** **Safety and constraints are inputs to the workflow, not obstacles around it.**

### 2) Slide-by-slide outline

#### Slide 1 — The constraint map (why enterprises differ)
- **Key bullets:**
  - Approved models only
  - No external SaaS uploads / no code paste policies
  - Auditability + security review cycles
- **Speaker notes:** Constraints aren’t “red tape”; they define what “good” looks like.
- **Visual:** Constraint triangle (Security / Compliance / Velocity).
- **Time:** 2 min

#### Slide 2 — Data classes: safe / redact / never
- **Key bullets:**
  - Safe: high-level architecture summaries, public docs, synthetic examples
  - Redact: logs, tickets, configs (remove identifiers/secrets)
  - Never: PHI/PII, credentials, proprietary customer data, production secrets
- **Speaker notes:** If you’re unsure, treat it as “redact” or “never” until confirmed.
- **Visual:** 3-column table.
- **Time:** 3 min

#### Slide 3 — “Context pack” concept (what you provide instead of raw code)
- **Key bullets:**
  - Intent + requirements + constraints
  - Interfaces/contracts + minimal snippets
  - Acceptance criteria + test expectations
- **Speaker notes:** The point is to enable good reasoning without exposing sensitive artifacts.
- **Visual:** “Context pack” checklist card.
- **Time:** 3 min

#### Slide 4 — Redaction rules of thumb (practical)
- **Key bullets:**
  - Replace identifiers with stable placeholders
  - Remove secrets; never “mask” with reversible patterns
  - Keep structure (shape matters more than exact values)
- **Speaker notes:** Preserve the *pattern* (schema, error shapes) while removing the *data*.
- **Visual:** Before/after redaction example block.
- **Time:** 3 min

#### Slide 5 — Approved tools/models (workflow implication)
- **Key bullets:**
  - Tool choice affects: context assembly, permissions, audit logs
  - Centralize policy: don’t rely on “developer memory”
  - Prefer repeatable templates over ad hoc prompts
- **Speaker notes:** Workflow should make the safe path the easy path.
- **Visual:** “Policy → Template → Output” pipeline.
- **Time:** 2 min

#### Slide 6 — Off-network coaching (conceptual)
- **Key bullets:**
  - Coaches don’t touch sensitive code directly
  - Coaching focuses on process, not secret artifacts
  - Learners apply guidance locally
- **Speaker notes:** This is common in regulated environments; it’s workable if artifacts are designed well.
- **Visual:** Coach (process) ↔ Learner (code) separation diagram.
- **Time:** 2 min

#### Slide 7 — Untrusted input boundary (setup for injection)
- **Key bullets:**
  - Tickets, docs, emails, web pages can contain adversarial text
  - Treat as *data*, not instructions
  - Isolate + label untrusted content
- **Speaker notes:** This is the core mental model behind prompt injection defenses.
- **Visual:** “Trusted instructions” vs “Untrusted data” split box.
- **Time:** 3 min

#### Slide 8 — Common misconceptions (callouts)
- **Key bullets:**
  - Misconception: “Redacting values makes any prompt safe”
  - Reality: structure can still leak; policies still apply
  - Misconception: “If it’s internal, it’s safe”
  - Reality: internal SaaS uploads can still violate policy/audit requirements
- **Speaker notes:** Safety is about *policy + threat model*, not intent.
- **Visual:** Two callout boxes.
- **Time:** 2–3 min

#### Slide 9 — Practical checklist (what to do on Monday)
- **Key bullets:**
  - Use a data classification checklist before prompting
  - Use context packs + contracts
  - Record decisions (audit notes) for sensitive work
- **Speaker notes:** The goal is speed with control: repeatable, reviewable, auditable.
- **Visual:** Checklist.
- **Time:** 2 min

### 3) Demo-in-lecture plan (no execution required)
- **Demo moment 1 (Slide 3–4):** Context pack + redaction example
  - **Snippet (on-slide):**
    ```text
    CONTEXT PACK (sanitized)
    - Service: ClaimsEligibility (C#/.NET)
    - Problem: intermittent 500s on POST /eligibility
    - Constraints: no PHI/PII in prompts; do not change DB schema
    - Evidence (redacted): request_id=REQ_123, error=TimeoutException at <REDACTED_HOST>
    - Output contract: Root cause hypotheses + minimal patch plan + tests
    ```
  - **What to point out:** You can ask for high-quality help without pasting secrets; constraints should be explicit.
  - **What could go wrong:** “Masking” secrets but leaving real endpoints/user IDs; including entire ticket dumps with untrusted instructions.

### 4) Examples bank
- **Good example:** “Given this sanitized context pack, propose 3 root-cause hypotheses + the smallest diagnostic change + tests.”
- **Bad example (why it fails):** “Here are production logs; tell me what to do.” (unsafe data exposure; no constraints)
- **Enterprise-safe example:** Use synthetic logs that preserve schema/timeouts; keep identifiers as placeholders.

### 5) Graphics pack (image/diagram prompts)
- **Infographic:** Data class table (safe / redact / never)
  - Prompt: “A simple 3-column enterprise table labeled Safe, Redact, Never; include 4–6 examples per column; clean typography.”
  - Nano Banana variant: “Minimal infographic with three columns and icons (check, scissors, stop).”
  - Label: infographic
  - Placement: Slide 2
- **Flowchart:** “Context pack” assembly checklist
  - Prompt: “A flowchart showing context assembly: constraints → requirements → minimal artifacts → acceptance criteria → output contract.”
  - Nano Banana variant: “Create a simple left-to-right flow diagram with 5 labeled boxes for context pack assembly.”
  - Label: flowchart
  - Placement: Slide 3

### 6) Safety & risk callouts
- **Relevant risks:** Sensitive data exposure; policy violations; untrusted input influencing actions.
- **Mitigations to mention:** Data classification; redaction; isolate untrusted content; require approvals for any action-like tools.
- **Critical safety concepts:** **Untrusted text must not drive tool actions** (foundation for prompt injection defense).

