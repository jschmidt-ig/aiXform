# Sessions 07–08 — Slide Outlines (Fundamentals)

## Session 7 — Prompting fundamentals

### 1) Session summary
- **Title:** Prompt anatomy: role, constraints, examples, acceptance criteria
- **Purpose (1 sentence):** Teach a repeatable prompt structure that produces reviewable, testable outputs (not vague prose).
- **Learning objectives (3):**
  1. Use a standard prompt “anatomy” that includes role + constraints + acceptance criteria.
  2. Write an output contract that limits ambiguity and scope creep.
  3. Recognize common prompt pitfalls (underspecified tasks, conflicting goals, missing constraints).
- **If learners only remember 1 thing:** **A good prompt is a spec: constraints + contract + checks.**

### 2) Slide-by-slide outline

#### Slide 1 — Prompting isn’t “magic words”
- **Key bullets:**
  - You’re specifying a task for a probabilistic system
  - Structure beats clever phrasing
  - The goal is *reviewable artifacts*
- **Speaker notes:** Think “requirements + template,” not “incantation.”
- **Visual:** “Spec mindset” icon + short definition.
- **Time:** 2–3 min

#### Slide 2 — Prompt anatomy (the repeatable template)
- **Key bullets:**
  - Role (what the model is)
  - Task (what to produce)
  - Constraints (what not to do)
  - Inputs (context pack)
  - Output contract (format)
  - Acceptance criteria (how we judge)
- **Speaker notes:** If your prompt is missing any of these, expect drift.
- **Visual:** Prompt anatomy checklist.
- **Time:** 3 min

#### Slide 3 — Constraints: the safety and scope guard
- **Key bullets:**
  - Explicit “do not” statements
  - Boundaries: no schema changes, no external SaaS, no secrets/PHI
  - “Ask clarifying questions if missing context”
- **Speaker notes:** Constraints are part of the spec, not an afterthought.
- **Visual:** Constraints card with red “must not” bullets.
- **Time:** 3 min

#### Slide 4 — Output contracts: turn prose into artifacts
- **Key bullets:**
  - Sections or structured fields
  - “Assumptions” and “uncertainties” required
  - Limits: max steps, max files touched, etc.
- **Speaker notes:** Contracts make it possible to grade and automate later.
- **Visual:** Contract template example.
- **Time:** 3 min

#### Slide 5 — Acceptance criteria: what “done” means
- **Key bullets:**
  - Observable checks (tests, lint, docs)
  - Non-functional constraints (performance, security)
  - “No behavior change” vs “intentional change”
- **Speaker notes:** If acceptance criteria are vague, the model will invent.
- **Visual:** “AC” checklist.
- **Time:** 2–3 min

#### Slide 6 — Examples: few-shot steering (when to use)
- **Key bullets:**
  - Show a “good” output snippet
  - Show a “bad” output snippet
  - Keep examples short; match the contract
- **Speaker notes:** Examples are the fastest way to set tone and granularity.
- **Visual:** Good vs bad snippet boxes.
- **Time:** 2 min

#### Slide 7 — Pitfalls checklist
- **Key bullets:**
  - Ambiguity (“improve”, “optimize”, “refactor”)
  - Conflicting goals (“fastest” + “safest” + “no changes”)
  - Missing inputs (no constraints, no context pack)
- **Speaker notes:** Most failures are prompt quality, not “model weakness.”
- **Visual:** “Prompt lint” checklist.
- **Time:** 2 min

#### Slide 8 — Common misconceptions (callouts)
- **Key bullets:**
  - Misconception: “Prompt engineering = secret phrasing”
  - Reality: clear specs + contracts + verification
  - Misconception: “More detail is always better”
  - Reality: irrelevant detail can poison context
- **Speaker notes:** We’ll formalize context engineering next week.
- **Visual:** Two callout boxes.
- **Time:** 2 min

#### Slide 9 — Takeaway: a reusable prompt template
- **Key bullets:**
  - Create a team prompt template library
  - Pair with context packs + redaction rules
  - Review prompts like code (iterate)
- **Speaker notes:** Mature teams treat prompting as an engineering surface.
- **Visual:** “Template library” folder icon.
- **Time:** 2 min

### 3) Demo-in-lecture plan (no execution required)
- **Demo moment 1 (Slide 2–4):** Before/after prompt transformation
  - **Snippet (on-slide):**
    ```text
    BEFORE: "Fix the logging in this service."

    AFTER (structured):
    ROLE: senior engineer
    TASK: propose a minimal change plan
    CONSTRAINTS: no PHI/PII; no schema changes; <=3 files
    INPUT: sanitized context pack
    OUTPUT CONTRACT: Assumptions / Plan / Risks / Tests
    ACCEPTANCE: adds correlation id; tests updated; no new deps
    ```
  - **What to point out:** The “after” is a spec; it narrows the solution space.
  - **What could go wrong:** Over-constraining early exploration; fix by allowing “questions first.”

### 4) Examples bank
- **Good example:** “Draft a PR description using this exact contract; include risk and test plan.”
- **Bad example (why it fails):** “Make it better.” (non-testable, encourages scope creep)
- **Enterprise-safe example:** Use sanitized interfaces and synthetic examples; request contracts, not raw code.

### 5) Graphics pack (image/diagram prompts)
- **Infographic:** Prompt anatomy checklist
  - Prompt: “A checklist infographic titled ‘Prompt Anatomy’ with 6 items (Role, Task, Constraints, Inputs, Output Contract, Acceptance Criteria).”
  - Nano Banana variant: “Minimal checklist card with 6 labeled rows and icons.”
  - Label: infographic
  - Placement: Slide 2
- **Table:** Prompt pitfalls (“prompt lint”)
  - Prompt: “A table titled ‘Prompt Lint’ listing pitfalls and fixes (ambiguity, conflicts, missing inputs).”
  - Nano Banana variant: “Minimal two-column table with ‘Problem’ and ‘Fix’.”
  - Label: infographic
  - Placement: Slide 7

### 6) Safety & risk callouts
- **Relevant risks:** Unsafe requests; accidental sensitive context; ambiguous prompts causing broad changes.
- **Mitigations to mention:** Explicit constraints; redaction rules; “ask questions first”; output contracts.
- **Critical safety concepts:** Constraints must be explicit; never request or include sensitive data.

---

## Session 8 — Chatbot vs raw model call

### 1) Session summary
- **Title:** What chat UIs hide: roles, context assembly, and safety wrappers
- **Purpose (1 sentence):** Build API-level intuition so learners can reason about agents/harnesses later (even if they mostly use chat/IDE tools).
- **Learning objectives (3):**
  1. Explain message roles (system/developer/user) and why they matter.
  2. Describe how a chatbot UI assembles context (hidden prompts, memory features, tools).
  3. Relate UI differences to reliability/safety (auditability, permissions, reproducibility).
- **If learners only remember 1 thing:** **A “chatbot” is a harness; the API mental model helps you stay in control.**

### 2) Slide-by-slide outline

#### Slide 1 — Same model, different harness behaviors
- **Key bullets:**
  - UI choices change outcomes (context, guardrails)
  - Hidden instructions exist in most products
  - Reproducibility depends on what’s actually sent
- **Speaker notes:** If you can’t describe the harness, you can’t debug it.
- **Visual:** Model at center with multiple harnesses around it.
- **Time:** 3 min

#### Slide 2 — Message roles (instruction hierarchy)
- **Key bullets:**
  - System: highest priority rules
  - Developer: app/tool constraints
  - User: the request
  - Untrusted content: *data*, not instructions
- **Speaker notes:** This hierarchy is crucial for injection defenses later.
- **Visual:** Pyramid or stack of roles.
- **Time:** 3 min

#### Slide 3 — What chat UIs often add
- **Key bullets:**
  - Safety policies and “helpfulness” defaults
  - Conversation summarization / memory features
  - Tool integrations (search, connectors)
- **Speaker notes:** Great UX can hide important knobs; don’t confuse UX with model capability.
- **Visual:** “UI wrapper” layer around a model.
- **Time:** 2–3 min

#### Slide 4 — API call mental model (conceptual)
- **Key bullets:**
  - You send messages + parameters
  - You receive a completion (tokens out)
  - You control exactly what context is included
- **Speaker notes:** This is the “truth” behind most harnesses.
- **Visual:** Request/response diagram.
- **Time:** 3 min

#### Slide 5 — Example: an API request (on-slide only)
- **Key bullets:**
  - Messages array with roles
  - Output contract request
  - No execution required
- **Speaker notes:** We’re not teaching a specific API; we’re teaching the pattern.
- **Visual:** Code block callout.
- **Time:** 3 min

#### Slide 6 — Reproducibility and auditability
- **Key bullets:**
  - Logs/transcripts enable review
  - Determinism is limited; inputs matter
  - Versioning prompts/contracts improves repeatability
- **Speaker notes:** In enterprises, “show your work” matters as much as results.
- **Visual:** “Transcript” document icon + audit trail arrows.
- **Time:** 2–3 min

#### Slide 7 — Common misconceptions (callouts)
- **Key bullets:**
  - Misconception: “Chat is simpler, so it’s safer”
  - Reality: hidden context can reduce auditability
  - Misconception: “API calls are only for ML engineers”
  - Reality: API-level thinking is a safety skill for everyone
- **Speaker notes:** You can use chat products *and* still think clearly about roles and context.
- **Visual:** Two callout boxes.
- **Time:** 2 min

#### Slide 8 — Takeaway: think in roles + working set
- **Key bullets:**
  - Always ask: what context is included?
  - Put constraints at the top (system/developer equivalent)
  - Isolate untrusted text as data
- **Speaker notes:** This becomes the foundation for tool calling and injection defense.
- **Visual:** “Working set” box + role labels.
- **Time:** 2 min

### 3) Demo-in-lecture plan (no execution required)
- **Demo moment 1 (Slide 5):** API request pattern (generic)
  - **Snippet (on-slide):**
    ```json
    {
      "messages": [
        {"role": "system", "content": "Follow enterprise safety rules."},
        {"role": "user", "content": "Draft a change plan using the contract below..."}
      ],
      "output_contract": ["Assumptions", "Plan", "Risks", "Tests"]
    }
    ```
  - **What to point out:** Roles separate rules from requests; the harness determines what’s included.
  - **What could go wrong:** Treating untrusted documents as “system instructions” (injection risk).

### 4) Examples bank
- **Good example:** “Given this role hierarchy, where would you put redaction rules and tool restrictions?”
- **Bad example (why it fails):** “Just remember our policy forever.” (relies on vague memory assumptions)
- **Enterprise-safe example:** Store policy templates in approved docs; re-provide them in every relevant interaction.

### 5) Graphics pack (image/diagram prompts)
- **Diagram:** Role hierarchy
  - Prompt: “A simple pyramid labeled System, Developer, User, Untrusted Content; show decreasing priority.”
  - Nano Banana variant: “Minimal stacked diagram with 4 layers and labels; add a shield icon near System.”
  - Label: infographic
  - Placement: Slide 2
- **Flowchart:** Request/response mental model
  - Prompt: “A request/response diagram: Messages + parameters → Model → Output tokens; clean enterprise style.”
  - Nano Banana variant: “Minimal two-box flow: Request → LLM → Response.”
  - Label: flowchart
  - Placement: Slide 4

### 6) Safety & risk callouts
- **Relevant risks:** Hidden context reducing auditability; accidental inclusion of sensitive data via “memory”; untrusted content treated as instructions.
- **Mitigations to mention:** Use explicit context packs; keep transcripts; isolate untrusted text; avoid relying on implicit memory.
- **Critical safety concepts:** Instruction hierarchy sets up prompt injection defenses.

