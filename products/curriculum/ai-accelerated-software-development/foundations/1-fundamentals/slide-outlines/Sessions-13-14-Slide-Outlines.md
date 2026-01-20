# Sessions 13–14 — Slide Outlines (Fundamentals)

## Session 13 — Agentic coding method (course focus)

### 1) Session summary
- **Title:** The method: plan → diff → test → narrate (and keep humans in control)
- **Purpose (1 sentence):** Teach a concrete, repeatable loop for AI-assisted coding that produces safe, reviewable PRs.
- **Learning objectives (3):**
  1. Apply the “plan → diff → test → narrate” method to a small change.
  2. Use contracts that force evidence (tests, risk notes, assumptions).
  3. State the principle: **never let the agent deploy**; approvals are required.
- **If learners only remember 1 thing:** **Demand evidence: diffs + tests + narration—not just an answer.**

### 2) Slide-by-slide outline

#### Slide 1 — Why method beats tool choice
- **Key bullets:**
  - Tools come and go; workflow persists
  - Method reduces thrash and risk
  - Works across chat/IDE/CLI harnesses
- **Speaker notes:** Method gives you leverage and makes teams consistent.
- **Visual:** Tool logos replaced by generic icons + a single method arrow.
- **Time:** 2–3 min

#### Slide 2 — The loop: plan → diff → test → narrate
- **Key bullets:**
  - Plan: constraints + steps + risks
  - Diff: minimal patch proposal
  - Test: evidence of correctness
  - Narrate: PR description for reviewers
- **Speaker notes:** If any step is missing, you’re operating on faith.
- **Visual:** 4-step loop.
- **Time:** 3 min

#### Slide 3 — Step 1: plan (what “good” looks like)
- **Key bullets:**
  - Ask clarifying questions first
  - Keep scope narrow (≤3 files as default)
  - Explicit risks and rollback notes
- **Speaker notes:** A plan is how you prevent scope creep and unsafe leaps.
- **Visual:** Plan template card.
- **Time:** 3 min

#### Slide 4 — Step 2: diff (small and reviewable)
- **Key bullets:**
  - Prefer minimal diffs
  - Preserve existing patterns
  - Explain why each change exists
- **Speaker notes:** Large diffs hide mistakes; small diffs accelerate review.
- **Visual:** “Small diff” illustration (few lines changed).
- **Time:** 2–3 min

#### Slide 5 — Step 3: test (evidence)
- **Key bullets:**
  - Unit tests for logic changes
  - Integration tests for contracts/boundaries
  - “What I didn’t test” is allowed—if stated
- **Speaker notes:** Testing is the strongest antidote to hallucination in code.
- **Visual:** Evidence checklist.
- **Time:** 3 min

#### Slide 6 — Step 4: narrate (PR narration)
- **Key bullets:**
  - What changed and why
  - Risks and mitigations
  - Testing performed
  - Out of scope
- **Speaker notes:** Narration is how you make AI-assisted work auditable.
- **Visual:** PR template.
- **Time:** 3 min

#### Slide 7 — Safety principle: never let the agent deploy
- **Key bullets:**
  - Deploy is high blast radius
  - Require human approval
  - Separate “propose” from “execute”
- **Speaker notes:** This is a hard safety line in most enterprises.
- **Visual:** “Deploy” tool with a red approval gate.
- **Time:** 2 min

#### Slide 8 — Common misconceptions (callouts)
- **Key bullets:**
  - Misconception: “If tests pass, it’s safe”
  - Reality: tests are necessary, not sufficient (review + risk)
  - Misconception: “AI will handle edge cases”
  - Reality: you must ask for edge cases explicitly and validate
- **Speaker notes:** Safety is multi-layer: tests + review + permissions.
- **Visual:** Two callout boxes.
- **Time:** 2 min

#### Slide 9 — Takeaway: make outputs reviewable by default
- **Key bullets:**
  - Standardize the loop as team practice
  - Version contracts and templates
  - Track metrics (cycle time, defects, rework)
- **Speaker notes:** This is how teams get consistent value and reduce anxiety.
- **Visual:** “Team standard” stamp.
- **Time:** 2 min

### 3) Demo-in-lecture plan (no execution required)
- **Demo moment 1 (Slide 2–6):** One mini-task through the loop
  - **Snippet (on-slide):**
    ```text
    TASK: Add correlation id to logs.
    PLAN: steps + risks + tests.
    DIFF: show 6-line pseudodiff.
    TEST: list 2 tests added/updated.
    NARRATE: PR template filled.
    ```
  - **What to point out:** Every step creates an artifact a reviewer can validate quickly.
  - **What could go wrong:** Skipping plan/narration leads to “mystery diffs” and mistrust.

### 4) Examples bank
- **Good example:** “Produce a patch proposal + tests + PR narration under this contract.”
- **Bad example (why it fails):** “Just commit the changes.” (unsafe; bypasses review/approval)
- **Enterprise-safe example:** Require human sign-off before write actions; keep deploy permissions fully separate.

### 5) Graphics pack (image/diagram prompts)
- **Diagram:** Plan → diff → test → narrate loop
  - Prompt: “A 4-step loop diagram labeled Plan, Diff, Test, Narrate; include small icons (clipboard, code, check, document).”
  - Nano Banana variant: “Minimal circular diagram with 4 labeled nodes and arrows; enterprise style.”
  - Label: flowchart
  - Placement: Slide 2
- **Infographic:** PR narration template
  - Prompt: “A clean PR template card with sections What, Why, Risk, Testing, Out of Scope.”
  - Nano Banana variant: “Minimal template card with headings and short bullet placeholders.”
  - Label: infographic
  - Placement: Slide 6

### 6) Safety & risk callouts
- **Relevant risks:** Over-trusting code changes; insufficient testing; unauthorized execution actions.
- **Mitigations to mention:** Artifact loop; explicit approvals; least privilege; audit logs.
- **Critical safety concepts:** **Never let the agent deploy**; approvals for write/deploy.

---

## Session 14 — Model mixing + harness comparisons

### 1) Session summary
- **Title:** Model selection: capability vs cost/latency vs risk
- **Purpose (1 sentence):** Give learners a decision framework for choosing models/harnesses for tasks without assuming a single “best model.”
- **Learning objectives (3):**
  1. Explain why model mixing is feasible (no durable memory by default).
  2. Choose a model/harness based on task type (ideation vs precision vs speed).
  3. Identify trade-offs: cost, latency, reliability, safety controls.
- **If learners only remember 1 thing:** **Pick models by task and constraints—not by hype.**

### 2) Slide-by-slide outline

#### Slide 1 — Why “one model for everything” fails
- **Key bullets:**
  - Different tasks have different requirements
  - Bigger isn’t always faster or safer
  - Contracts and verification reduce dependence on model quality
- **Speaker notes:** Your workflow can make smaller models usable for many tasks.
- **Visual:** Task types mapped to different model sizes.
- **Time:** 3 min

#### Slide 2 — Model mixing is possible because memory is limited
- **Key bullets:**
  - No durable memory by default
  - You can move artifacts between runs (contracts)
  - The workflow holds state, not the model
- **Speaker notes:** Artifacts are the handoff mechanism: plans, diffs, tests, narration.
- **Visual:** Artifacts flowing between “Model A” and “Model B.”
- **Time:** 3 min

#### Slide 3 — Decision tree: which model for which task
- **Key bullets:**
  - Ideation/brainstorming: fast/cheap is fine
  - Precise edits: higher reliability preferred
  - Safety-sensitive tasks: prioritize guardrails + review, not autonomy
- **Speaker notes:** The decision tree should be simple enough to follow under pressure.
- **Visual:** Decision tree.
- **Time:** 4 min

#### Slide 4 — Harness factors that matter as much as model
- **Key bullets:**
  - Context access (repo, docs, tickets)
  - Tool power and permissions
  - Audit logs and reproducibility
- **Speaker notes:** A weaker model in a better harness can outperform a stronger model in a worse harness.
- **Visual:** 3-factor radar chart (conceptual).
- **Time:** 3 min

#### Slide 5 — Risk lens: bigger models aren’t inherently safer
- **Key bullets:**
  - More capability can mean more dangerous tool use
  - Safety is a workflow property (permissions + approvals)
  - Always isolate untrusted inputs
- **Speaker notes:** Safety depends on what actions are allowed, not on the model name.
- **Visual:** “Capability ↑ → potential blast radius ↑” graph.
- **Time:** 3 min

#### Slide 6 — Common misconceptions (callouts)
- **Key bullets:**
  - Misconception: “Model mixing is confusing and unreliable”
  - Reality: contracts and artifacts make it manageable
  - Misconception: “Pick the biggest model for production changes”
  - Reality: pick the safest workflow; model is secondary
- **Speaker notes:** Normalize using different tools for different steps.
- **Visual:** Two callout boxes.
- **Time:** 2 min

#### Slide 7 — Takeaway: standardize on artifacts
- **Key bullets:**
  - Plans, diffs, tests, narration are the stable interface
  - Model choice becomes a swap, not a dependency
  - Measure outcomes (quality, speed, incidents)
- **Speaker notes:** Artifacts are the interoperability layer across tools and teams.
- **Visual:** “Artifact interface” diagram.
- **Time:** 2 min

### 3) Demo-in-lecture plan (no execution required)
- **Demo moment 1 (Slide 3):** Apply decision tree to 3 tasks
  - **Snippet (on-slide):**
    ```text
    Task A: brainstorm lab exercises -> fast model
    Task B: draft PR narration -> reliable model
    Task C: propose tool permissions -> safety-first workflow + human review
    ```
  - **What to point out:** The model choice follows the task constraints; safety tasks always require explicit gates.
  - **What could go wrong:** Learners treat “fast model” as “sloppy output”—contracts still apply.

### 4) Examples bank
- **Good example:** “Choose a model/harness for writing a test plan vs editing code; justify.”
- **Bad example (why it fails):** “Use whatever model is newest.” (no decision criteria)
- **Enterprise-safe example:** Use smaller models for summaries; reserve higher-capability models for constrained tasks with review.

### 5) Graphics pack (image/diagram prompts)
- **Decision tree:** Model selection
  - Prompt: “A simple decision tree for model selection based on task type (ideation, precision edits, safety-sensitive).”
  - Nano Banana variant: “Minimal decision tree with 3 leaves; add icons (lightbulb, wrench, shield).”
  - Label: flowchart
  - Placement: Slide 3
- **Diagram:** Artifacts as interoperability layer
  - Prompt: “A diagram showing artifacts (plan/diff/tests/narration) as a shared interface between multiple models/harnesses.”
  - Nano Banana variant: “Minimal diagram: Model A → Artifacts → Model B; artifacts in a central box.”
  - Label: flowchart
  - Placement: Slide 2 or 7

### 6) Safety & risk callouts
- **Relevant risks:** Tool misuse by high-capability models; over-trusting “stronger” outputs; inconsistent workflows.
- **Mitigations to mention:** Standard artifacts; approval gates; least privilege; validation.
- **Critical safety concepts:** Safety is determined by permissions + review, not model capability.

