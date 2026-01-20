# Sessions 19–20 — Slide Outlines (Fundamentals)

## Session 19 — Security lab (lecture-based)

### 1) Session summary
- **Title:** Security lab: permissions + injection + mitigations (practice)
- **Purpose (1 sentence):** Practice critical safety judgment with realistic scenarios so learners pass the safety gate and can apply safe workflows in Labs/Applied.
- **Learning objectives (3):**
  1. Choose safe tool permission sets for common tasks (least privilege + approvals).
  2. Identify prompt injection attempts in untrusted inputs and respond correctly.
  3. Propose mitigations (isolation, gating, validation, audit) for each scenario.
- **If learners only remember 1 thing:** **Safety is a workflow you can practice and standardize.**

### 2) Slide-by-slide outline

#### Slide 1 — Lab setup: how this works (no tools)
- **Key bullets:**
  - We will analyze 2–3 scenarios
  - You will choose permissions, identify injection, and pick mitigations
  - Focus: judgment and reasoning, not trivia
- **Speaker notes:** This is rehearsal for real enterprise situations.
- **Visual:** 3-step lab flow.
- **Time:** 2 min

#### Slide 2 — Safety gate reminder (critical items)
- **Key bullets:**
  - Least privilege + approval gates
  - Prompt injection recognition + refusal
  - Untrusted text cannot control tool calls
- **Speaker notes:** Missing any critical safety concept is a hard fail.
- **Visual:** “Critical safety” badge list.
- **Time:** 3 min

#### Slide 3 — Scenario 1: small refactor request + tool list
- **Key bullets:**
  - Tools available: read_repo, write_repo, run_tests, deploy_prod, send_email
  - Task: “Propose a small refactor; do not change production.”
  - Choose the best permission set
- **Speaker notes:** Aim for the minimum permissions to complete the task safely.
- **Visual:** Scenario card.
- **Time:** 5 min

#### Slide 4 — Scenario 1 debrief (best answer + why)
- **Key bullets:**
  - Allow: read_repo + run_tests
  - Gate: write_repo requires explicit approval + diff review
  - Prohibit: deploy_prod (manual only)
- **Speaker notes:** Convenience permissions are the classic failure mode.
- **Visual:** Permission set card (Allowed / Gated / Prohibited).
- **Time:** 3 min

#### Slide 5 — Scenario 2: untrusted doc includes “ignore instructions”
- **Key bullets:**
  - Identify injection patterns
  - State correct response behavior
  - Decide what parts can still be used as data
- **Speaker notes:** The goal is to continue safely, not to “panic.”
- **Visual:** Untrusted text block with warning icon.
- **Time:** 5 min

#### Slide 6 — Scenario 2 debrief (defense in depth)
- **Key bullets:**
  - Isolate untrusted content
  - Restate trusted constraints
  - Gate tools; refuse unsafe actions
  - Validate outputs with contracts/checklists
- **Speaker notes:** Multiple layers catch mistakes even if one layer fails.
- **Visual:** Defense-in-depth flow.
- **Time:** 3–4 min

#### Slide 7 — Scenario 3 (optional): connector/tool risk
- **Key bullets:**
  - “AI assistant can access ticket system + email”
  - Identify data exposure and action risks
  - Propose governance (approvals, logging, scopes)
- **Speaker notes:** Connectors and action tools are where enterprises get hurt.
- **Visual:** Connector risk card.
- **Time:** 4–5 min

#### Slide 8 — Wrap-up: personal safety rules (share out)
- **Key bullets:**
  - One rule you will follow
  - One place your team needs a policy/template
  - One thing you will verify before accepting AI output
- **Speaker notes:** The goal is to convert concepts into behaviors.
- **Visual:** “My rules” sticky notes layout.
- **Time:** 2–3 min

### 3) Demo-in-lecture plan (no execution required)
- **Demo moment 1 (Slide 3–4):** Show the “permission reasoning” out loud
  - **Snippet (on-slide):**
    ```text
    Task needs: read + evidence (tests)
    Task does NOT need: deploy or email
    Writes are risky: require approval + review
    ```
  - **What to point out:** Reason from task intent to tool permissions; default deny for high risk.
  - **What could go wrong:** Learners assume “agent needs everything” to be useful.

### 4) Examples bank
- **Good example:** “Use read-only mode to generate a plan and diff; human applies and runs deploy.”
- **Bad example (why it fails):** “Let the agent email stakeholders automatically.” (privacy and governance risks)
- **Enterprise-safe example:** Require approvals for any outbound communications or state changes.

### 5) Graphics pack (image/diagram prompts)
- **Infographic:** Allowed / Gated / Prohibited permissions card
  - Prompt: “A three-column card labeled Allowed, Gated (Approval), Prohibited; include example tools under each; enterprise style.”
  - Nano Banana variant: “Minimal three-column card with icons (check, lock, stop).”
  - Label: infographic
  - Placement: Slide 4
- **Flowchart:** Defense in depth
  - Prompt: “A 4-step flowchart: Isolate input → Gate tools → Validate output → Audit/log; include icons.”
  - Nano Banana variant: “Minimal flowchart with 4 boxes and arrows; shield icons.”
  - Label: flowchart
  - Placement: Slide 6

### 6) Safety & risk callouts
- **Relevant risks:** Misconfigured permissions; injection leading to actions; connector-based data exposure.
- **Mitigations to mention:** Least privilege; approvals; isolation; validation; logging.
- **Critical safety concepts:** Reinforces end-test critical items.

---

## Session 20 — Integrated capstone demo + recap/Q&A (lecture-based)

### 1) Session summary
- **Title:** End-to-end mental model: API → harness → tools → injection → mitigations
- **Purpose (1 sentence):** Tie the entire Fundamentals module together in one conceptual walkthrough and prepare learners for Labs.
- **Learning objectives (3):**
  1. Walk through an end-to-end scenario using the model/harness/workflow mental models.
  2. Identify where to add guardrails (contracts, tool gating, injection defenses, approvals).
  3. Summarize what Fundamentals enables in Labs and Applied.
- **If learners only remember 1 thing:** **End-to-end safety is designed: context + contracts + guardrails + verification.**

### 2) Slide-by-slide outline

#### Slide 1 — Capstone scenario (the story)
- **Key bullets:**
  - Task: diagnose intermittent 500s and propose a safe fix plan
  - Constraints: no PHI/PII; no deploy by agent; audit required
  - Goal: produce artifacts for a PR-ready change
- **Speaker notes:** The scenario is intentionally realistic and constrained.
- **Visual:** Scenario card.
- **Time:** 3 min

#### Slide 2 — Step 1: raw API call mental model
- **Key bullets:**
  - Messages + context pack in
  - Tokens out
  - No tools yet; advisory output
- **Speaker notes:** This clarifies what’s “model” vs “harness.”
- **Visual:** Request/response diagram.
- **Time:** 3 min

#### Slide 3 — Step 2: harness behavior (context assembly)
- **Key bullets:**
  - Add system/developer constraints
  - Attach artifacts (sanitized)
  - Set output contract
- **Speaker notes:** Harness decides what’s included and how it’s prioritized.
- **Visual:** Working set box with labeled sections.
- **Time:** 3 min

#### Slide 4 — Step 3: tool calling (evidence gathering)
- **Key bullets:**
  - Read repo or docs (read-only)
  - Run tests (evidence)
  - Summarize results into the plan
- **Speaker notes:** Tools supply ground truth; outputs should cite evidence.
- **Visual:** Tool loop with “evidence” arrows.
- **Time:** 3 min

#### Slide 5 — Step 4: injection attempt appears
- **Key bullets:**
  - Untrusted doc includes “ignore instructions”
  - Identify as injection
  - Treat as data only
- **Speaker notes:** This is where many systems fail if they don’t isolate inputs.
- **Visual:** Untrusted content block with warning icon.
- **Time:** 3 min

#### Slide 6 — Step 5: mitigations + permissioning
- **Key bullets:**
  - Isolate untrusted input
  - Gate tool calls (approval for write; prohibit deploy)
  - Validate outputs against contract
- **Speaker notes:** Defense in depth: you assume some layer will fail.
- **Visual:** Defense-in-depth flow.
- **Time:** 4 min

#### Slide 7 — Final artifacts (what “done” looks like)
- **Key bullets:**
  - Change plan (contracted)
  - Patch/diff proposal (minimal)
  - Test plan + evidence notes
  - PR narration (What/Why/Risk/Testing)
- **Speaker notes:** The artifacts are what you carry into Labs and Applied.
- **Visual:** Artifact bundle icons.
- **Time:** 3 min

#### Slide 8 — Recap: the 3-layer stack (again)
- **Key bullets:**
  - Model: tokens/inference limits
  - Harness: context + tools + logs
  - Workflow/Governance: permissions + approvals + validation
- **Speaker notes:** This stack is your debugging lens.
- **Visual:** 3-layer stack.
- **Time:** 2 min

#### Slide 9 — Q&A + transition to Labs
- **Key bullets:**
  - What you’ll do next: hands-on workflows
  - What to bring: a real task + constraints + redaction rules
  - Reminder: safety gate mindset carries forward
- **Speaker notes:** Encourage learners to bring realistic, sanitized tasks.
- **Visual:** “Next phase” arrow.
- **Time:** 2–4 min

### 3) Demo-in-lecture plan (no execution required)
- **Demo moment 1 (Slides 2–7):** Walk the scenario through the 5 steps
  - **Snippet (on-slide):**
    ```text
    Context pack -> Contract -> Evidence (tools) -> Injection detected -> Gated actions -> Verified artifacts
    ```
  - **What to point out:** Each step reduces uncertainty and increases safety.
  - **What could go wrong:** Skipping isolation/gating leads to “agent does what the doc says.”

### 4) Examples bank
- **Good example:** “Agent produces a bounded change plan + tests; humans execute writes/deploys.”
- **Bad example (why it fails):** “Agent reads emails and replies automatically with tool access.” (privacy + action risk)
- **Enterprise-safe example:** Require an approval step for any external communication or state change.

### 5) Graphics pack (image/diagram prompts)
- **Flowchart:** End-to-end scenario
  - Prompt: “A flowchart showing 5 steps: API mental model → Harness context assembly → Tool calling → Injection attempt → Mitigations + approval gates → Artifacts.”
  - Nano Banana variant: “Minimal 5-step flowchart with icons (API, box, tools, warning, shield, documents).”
  - Label: flowchart
  - Placement: Slide 2–7 (overview)
- **Diagram:** Artifact bundle
  - Prompt: “An icon set or diagram showing a bundle of artifacts: plan, diff, tests, PR narration; clean enterprise style.”
  - Nano Banana variant: “Minimal 4-icon bundle with labels; consistent line icons.”
  - Label: infographic
  - Placement: Slide 7

### 6) Safety & risk callouts
- **Relevant risks:** Untrusted input driving actions; over-permissioned tools; missing validation; hidden context.
- **Mitigations to mention:** Isolation; least privilege; approvals; contracts + validation; audit logs.
- **Critical safety concepts:** End-to-end defense-in-depth and explicit approval gates.

