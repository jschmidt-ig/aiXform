# Sessions 09–10 — Slide Outlines (Fundamentals)

## Session 9 — Prompt contracts + output schemas (lecture-only)

### 1) Session summary
- **Title:** Output contracts: reproducibility, automation, and safety
- **Purpose (1 sentence):** Show how structured outputs reduce ambiguity, enable validation, and prevent unsafe “freeform” behavior.
- **Learning objectives (3):**
  1. Explain why contracts matter (grading, automation, reproducibility, safety).
  2. Choose an appropriate contract type (sections vs key-value vs schema-like JSON).
  3. Validate outputs without running code (checklists and spot checks).
- **If learners only remember 1 thing:** **Contracts turn AI outputs into engineering artifacts you can verify.**

### 2) Slide-by-slide outline

#### Slide 1 — Why contracts exist (real reasons)
- **Key bullets:**
  - Stable structure across runs/tools
  - Enables automation later (parsing, linting)
  - Makes review faster and safer
- **Speaker notes:** Contracts are the bridge from “chat” to “workflow.”
- **Visual:** “Freeform” vs “Contracted” pipeline.
- **Time:** 3 min

#### Slide 2 — Contract types (a simple taxonomy)
- **Key bullets:**
  - Sectioned Markdown (fastest)
  - Key-value templates (semi-structured)
  - Schema-like JSON (strict; when needed)
- **Speaker notes:** Start with sections; move to strict schemas when automation demands it.
- **Visual:** 3-level ladder of structure.
- **Time:** 3 min

#### Slide 3 — Example contract: change plan
- **Key bullets:**
  - Assumptions
  - Plan (≤5 steps)
  - Risks (≥3)
  - Tests (unit/integration)
  - Rollout/rollback notes
- **Speaker notes:** This contract is broadly reusable across teams.
- **Visual:** Contract card.
- **Time:** 3 min

#### Slide 4 — Example contract: PR narration
- **Key bullets:**
  - What / Why / Risk / Testing
  - Links to evidence (tests, logs)
  - Explicit “out of scope” line
- **Speaker notes:** PR narration forces clarity and reduces reviewer burden.
- **Visual:** PR description template.
- **Time:** 2–3 min

#### Slide 5 — What “schema” means here (conceptual)
- **Key bullets:**
  - Field names and allowed values
  - Required vs optional fields
  - Constraints like max lengths
- **Speaker notes:** You don’t need a parser today; you need the mental model.
- **Visual:** Simple JSON schema-like box.
- **Time:** 3 min

#### Slide 6 — Validation without code (checklists)
- **Key bullets:**
  - Does it follow the contract exactly?
  - Are assumptions explicit and plausible?
  - Are risks actionable and mitigated?
  - Does the test plan match the change?
- **Speaker notes:** Validation is the missing step in most “AI-assisted” workflows.
- **Visual:** Review checklist.
- **Time:** 3 min

#### Slide 7 — Common misconceptions (callouts)
- **Key bullets:**
  - Misconception: “Contracts restrict creativity”
  - Reality: they restrict *ambiguity*; exploration can happen before contracting
  - Misconception: “JSON = better”
  - Reality: strict schemas add friction; use when you need automation
- **Speaker notes:** Don’t over-engineer; match structure to need.
- **Visual:** Two callout boxes.
- **Time:** 2 min

#### Slide 8 — Takeaway: build a contract library
- **Key bullets:**
  - 5–10 reusable contracts for common tasks
  - Version them like code
  - Pair with “prompt lint” rules
- **Speaker notes:** This is how teams scale safe AI usage.
- **Visual:** Library shelf icon with labeled templates.
- **Time:** 2 min

### 3) Demo-in-lecture plan (no execution required)
- **Demo moment 1 (Slide 3):** Two outputs, one contract
  - **Snippet (on-slide):**
    ```text
    Contract requires: Assumptions / Plan / Risks / Tests
    Output A: includes all sections (good)
    Output B: missing Risks and Tests (reject)
    ```
  - **What to point out:** Missing sections are a “fail fast”; you don’t debate quality until structure is met.
  - **What could go wrong:** Learners accept partially formatted outputs and then build on shaky ground.

### 4) Examples bank
- **Good example:** “Generate a PR description using the PR narration contract; include an ‘out of scope’ line.”
- **Bad example (why it fails):** “Write a PR description.” (no structure; hides risk/testing)
- **Enterprise-safe example:** Require a “data handling” section when relevant (what was included/excluded from AI context).

### 5) Graphics pack (image/diagram prompts)
- **Infographic:** Contract taxonomy ladder
  - Prompt: “A 3-step ladder labeled Sectioned Markdown, Key-Value Template, Schema-like JSON; include pros/cons.”
  - Nano Banana variant: “Minimal ladder infographic with 3 rungs and small icons.”
  - Label: infographic
  - Placement: Slide 2
- **Checklist card:** Output validation
  - Prompt: “A checklist card titled ‘Validate the Output’ with 6 short items; enterprise style.”
  - Nano Banana variant: “Minimal checklist card with check icons and short labels.”
  - Label: infographic
  - Placement: Slide 6

### 6) Safety & risk callouts
- **Relevant risks:** Format drift hiding unsafe actions; missing risks/tests leading to unsafe merges.
- **Mitigations to mention:** Contracts + validation checklists; require explicit risk and test sections.
- **Critical safety concepts:** Validation is part of safety; don’t treat AI output as “approved.”

---

## Session 10 — Context engineering workshop (lecture-only)

### 1) Session summary
- **Title:** Context engineering: building the “working set” on purpose
- **Purpose (1 sentence):** Give learners concrete patterns for assembling context so models produce reliable outputs without dumping sensitive or irrelevant data.
- **Learning objectives (3):**
  1. Assemble a context pack with correct ordering (constraints first, then artifacts).
  2. Apply “context budget” thinking: what to include/omit and why.
  3. Prevent context poisoning: isolate untrusted text and label it as data.
- **If learners only remember 1 thing:** **Curated context beats more context.**

### 2) Slide-by-slide outline

#### Slide 1 — Context engineering definition
- **Key bullets:**
  - Designing what the model sees
  - Ordering and compression matter
  - It’s a team skill, not an individual trick
- **Speaker notes:** Context engineering is “requirements engineering for AI inputs.”
- **Visual:** “Working set” box with labeled sections.
- **Time:** 2–3 min

#### Slide 2 — The context pack template (repeatable)
- **Key bullets:**
  - Constraints + redaction rules
  - Task + acceptance criteria
  - Minimal artifacts (interfaces, error shapes)
  - Output contract
- **Speaker notes:** This template will carry into Labs and Applied.
- **Visual:** Template card.
- **Time:** 3 min

#### Slide 3 — Ordering patterns (default and when to invert)
- **Key bullets:**
  - Default: summary/constraints → artifacts → examples
  - Invert when: you need a concrete example to anchor behavior
  - Always keep “must not” near the top
- **Speaker notes:** Order is a control surface; use it intentionally.
- **Visual:** Two example prompt skeletons with different ordering.
- **Time:** 3 min

#### Slide 4 — Context budget (token spend)
- **Key bullets:**
  - Spend tokens on constraints and interfaces
  - Don’t spend on irrelevant history
  - Keep “slack” for model reasoning/output
- **Speaker notes:** If you fill the window, you’ve removed room to think/answer.
- **Visual:** Budget bar.
- **Time:** 2–3 min

#### Slide 5 — Compression strategies
- **Key bullets:**
  - Summarize long docs into bullet facts
  - Include counts and shapes, not raw dumps
  - Use consistent placeholders
- **Speaker notes:** Compression should preserve decision-relevant details.
- **Visual:** Before/after: raw log dump vs summary.
- **Time:** 3 min

#### Slide 6 — Context poisoning (what it is)
- **Key bullets:**
  - Untrusted text can contain instructions
  - It can override or distract the model
  - Fix: isolate, label, and constrain
- **Speaker notes:** This is the bridge to prompt injection defenses.
- **Visual:** “Trusted instructions” and “Untrusted data” compartments.
- **Time:** 3 min

#### Slide 7 — Workshop example (walkthrough)
- **Key bullets:**
  - Start with a vague task
  - Add constraints + acceptance criteria
  - Add minimal artifacts
  - Add output contract
- **Speaker notes:** The point is to show the transformation process.
- **Visual:** Stepwise build-up (4 steps).
- **Time:** 4 min

#### Slide 8 — Common misconceptions (callouts)
- **Key bullets:**
  - Misconception: “Just paste the whole ticket/thread”
  - Reality: summarize + isolate untrusted parts
  - Misconception: “More logs = better answers”
  - Reality: structured summaries beat dumps
- **Speaker notes:** This is one of the biggest “Monday morning” behavior changes.
- **Visual:** Two callout boxes.
- **Time:** 2 min

#### Slide 9 — Takeaway: context pack = reusable asset
- **Key bullets:**
  - Build reusable system summaries (approved)
  - Standardize redaction + placeholders
  - Keep a contract library
- **Speaker notes:** Teams that do this well get compounding returns.
- **Visual:** “Reusable assets” triad.
- **Time:** 2 min

### 3) Demo-in-lecture plan (no execution required)
- **Demo moment 1 (Slide 7):** Build a context pack live (on slides)
  - **Snippet (on-slide):**
    ```text
    TASK: "Reduce flaky tests."
    CONSTRAINTS: no new deps; keep runtime stable; no PHI/PII.
    ARTIFACTS: list of 3 flaky tests + failure patterns (summarized).
    CONTRACT: Hypotheses / Minimal fixes / Risks / Tests.
    ```
  - **What to point out:** The context pack narrows the solution space and forces verification.
  - **What could go wrong:** Learners include full test logs with untrusted content; missing acceptance criteria leads to “rewrite everything.”

### 4) Examples bank
- **Good example:** “Given these 3 summarized flaky patterns, propose the smallest stabilization changes + tests.”
- **Bad example (why it fails):** “Here’s 5k lines of CI output.” (truncation; no structure)
- **Enterprise-safe example:** Provide anonymized test names and failure categories; no environment secrets.

### 5) Graphics pack (image/diagram prompts)
- **Infographic:** Context pack template card
  - Prompt: “A single-page template card labeled Constraints, Task, Artifacts, Output Contract; clean enterprise design.”
  - Nano Banana variant: “Minimal template card with 4 sections and icons.”
  - Label: infographic
  - Placement: Slide 2
- **Diagram:** Trusted vs untrusted compartments
  - Prompt: “A diagram showing a prompt split into two compartments: Trusted Instructions and Untrusted Data; untrusted is clearly labeled.”
  - Nano Banana variant: “Two-box diagram with a thick border around Trusted; Untrusted has a warning icon.”
  - Label: flowchart
  - Placement: Slide 6

### 6) Safety & risk callouts
- **Relevant risks:** Accidental sensitive data inclusion; untrusted text poisoning context; truncation removing constraints.
- **Mitigations to mention:** Summarize; isolate untrusted content; constraints-first ordering; context budgets.
- **Critical safety concepts:** **Isolate untrusted inputs** (foundation for injection defenses).

