# Sessions 11–12 — Slide Outlines (Fundamentals)

## Session 11 — Agents vs workflows + agentic loop

### 1) Session summary
- **Title:** Agents: LLM + tools + loop + objectives (and why that’s risky)
- **Purpose (1 sentence):** Help learners distinguish “agentic workflow” from “just chat,” and understand where autonomy fails without guardrails.
- **Learning objectives (3):**
  1. Define an agent and the agentic loop (plan → act → observe → reflect → iterate).
  2. Identify common agent failure modes (goal drift, tool misuse, brittle plans, context poisoning).
  3. Apply a “safe loop” checklist (least privilege, approvals, validation).
- **If learners only remember 1 thing:** **An agent is a workflow with autonomy—guardrails decide whether it helps or harms.**

### 2) Slide-by-slide outline

#### Slide 1 — Agent definition (simple and concrete)
- **Key bullets:**
  - Agent = model + tools + loop + objective
  - Autonomy exists on a spectrum
  - More autonomy increases both capability and risk
- **Speaker notes:** “Agent” is not a product; it’s an architecture pattern.
- **Visual:** 4-part agent definition diagram.
- **Time:** 3 min

#### Slide 2 — The agentic loop
- **Key bullets:**
  - Plan: decide next step
  - Act: call a tool / write an artifact
  - Observe: read results
  - Reflect: update plan
  - Iterate until done/stop
- **Speaker notes:** This loop is powerful—and where safety must be inserted.
- **Visual:** Loop diagram with arrows.
- **Time:** 3 min

#### Slide 3 — What agents add vs workflows
- **Key bullets:**
  - Workflows: fixed steps, predictable outputs
  - Agents: adaptive steps, variable paths
  - Choose the least autonomy that solves the task
- **Speaker notes:** Prefer workflows when the path is known; agents when discovery is needed.
- **Visual:** Autonomy spectrum (workflow → semi-agent → agent).
- **Time:** 3 min

#### Slide 4 — Failure mode: goal drift
- **Key bullets:**
  - Agent “helpfully” changes scope
  - Optimizes for completion over correctness
  - Fix: explicit constraints + stop conditions
- **Speaker notes:** The model is rewarded for finishing; you must define “finish safely.”
- **Visual:** Drift arrow away from scope box.
- **Time:** 3 min

#### Slide 5 — Failure mode: tool misuse
- **Key bullets:**
  - Wrong tool at wrong time
  - Unsafe tool permissions
  - Fix: least privilege + approvals + allowlists
- **Speaker notes:** Tool access turns text mistakes into real-world mistakes.
- **Visual:** Permission ladder (read → test → write → deploy).
- **Time:** 3 min

#### Slide 6 — Failure mode: brittle plans
- **Key bullets:**
  - Plan assumes facts not in evidence
  - Doesn’t adapt to tool results
  - Fix: “evidence required” checkpoints
- **Speaker notes:** Good agents treat tool results as ground truth and revise.
- **Visual:** Plan with checkpoints (“verify before proceed”).
- **Time:** 2–3 min

#### Slide 7 — The “safe loop” checklist
- **Key bullets:**
  - Start with a plan and constraints
  - Use read-only tools first
  - Require approval before write/deploy
  - Validate outputs (contracts + tests)
  - Stop if uncertainty is high
- **Speaker notes:** This is the minimum viable safety bar.
- **Visual:** Checklist card.
- **Time:** 3 min

#### Slide 8 — Common misconceptions (callouts)
- **Key bullets:**
  - Misconception: “Agents replace engineers”
  - Reality: engineers become supervisors/reviewers
  - Misconception: “More autonomy = faster”
  - Reality: more autonomy can increase rework and risk
- **Speaker notes:** Autonomy must be earned through guardrails and evidence.
- **Visual:** Two callout boxes.
- **Time:** 2 min

#### Slide 9 — Takeaway: design for “proof, not persuasion”
- **Key bullets:**
  - Prefer evidence (tests, diffs, logs)
  - Contracts enforce completeness
  - Human approval gates prevent catastrophic actions
- **Speaker notes:** Agents should produce artifacts you can verify quickly.
- **Visual:** “Evidence pipeline” (plan → diff → tests → narration).
- **Time:** 2 min

### 3) Demo-in-lecture plan (no execution required)
- **Demo moment 1 (Slide 2 or 7):** Annotated agent loop with guardrails
  - **Snippet (on-slide):**
    ```text
    LOOP:
    Plan -> (requires: constraints + output contract)
    Act  -> (allowed: read_repo, run_tests)
    Observe -> (must: cite evidence)
    Reflect -> (update plan; stop if uncertain)
    Write/Deploy -> (blocked without human approval)
    ```
  - **What to point out:** Guardrails are inserted at tool boundaries and decision points.
  - **What could go wrong:** Learners treat “agent” as a black box and skip evidence checkpoints.

### 4) Examples bank
- **Good example:** “Agent proposes a patch + tests; human reviews diff and evidence; merge only after checks.”
- **Bad example (why it fails):** “Agent has deploy permissions by default.” (catastrophic blast radius)
- **Enterprise-safe example:** Read-only agent in early adoption; graduate permissions slowly with audit logging.

### 5) Graphics pack (image/diagram prompts)
- **Diagram:** Agent definition (model + tools + loop + objective)
  - Prompt: “A clean diagram with four labeled components: Model, Tools, Loop, Objective; connected in a simple layout.”
  - Nano Banana variant: “Minimal icon-based diagram: brain, wrench, loop arrows, target.”
  - Label: infographic
  - Placement: Slide 1
- **Flowchart:** Agentic loop with guardrails
  - Prompt: “A circular loop diagram Plan → Act → Observe → Reflect with guardrail callouts (approval gate, least privilege, validation).”
  - Nano Banana variant: “Circular flowchart with 4 nodes and 3 small shield icons marking guardrails.”
  - Label: flowchart
  - Placement: Slide 2 or 7

### 6) Safety & risk callouts
- **Relevant risks:** Tool misuse; goal drift; untrusted input steering actions; hidden data exposure through tools.
- **Mitigations to mention:** Least privilege; approvals; allowlists; validation; stop conditions.
- **Critical safety concepts:** **Do not grant action tools without explicit approval gates** (reinforced later).

---

## Session 12 — Harness taxonomy

### 1) Session summary
- **Title:** Harnesses: chatbot vs IDE assistant vs CLI agent vs cloud agent
- **Purpose (1 sentence):** Give learners a practical taxonomy so they can reason about capabilities, risks, and auditability across tools.
- **Learning objectives (3):**
  1. Compare harness types by context access, tool surface, and permissions.
  2. Explain why auditability and reproducibility matter in enterprise settings.
  3. Identify where each harness commonly fails (missing context, unsafe tool use, poor logging).
- **If learners only remember 1 thing:** **Harness choice changes context, permissions, and audit—so it changes risk.**

### 2) Slide-by-slide outline

#### Slide 1 — What is a “harness”?
- **Key bullets:**
  - The wrapper around the model
  - Assembles context and tools
  - Enforces (or fails to enforce) policies
- **Speaker notes:** Harnesses are where enterprise constraints get implemented.
- **Visual:** Model in center; harness ring around it.
- **Time:** 2–3 min

#### Slide 2 — The harness landscape (taxonomy)
- **Key bullets:**
  - Chat UI
  - IDE assistant
  - CLI agent
  - Cloud agent
- **Speaker notes:** These categories differ mainly in tool access and context assembly.
- **Visual:** 2x2 grid: Context Access vs Tool Power.
- **Time:** 3 min

#### Slide 3 — Comparison table (what differs)
- **Key bullets:**
  - Context sources (chat history, repo, tickets, docs)
  - Tool actions (read, write, run, deploy)
  - Approval flow + audit logs
- **Speaker notes:** The same model can look “better” in one harness because context is richer.
- **Visual:** Comparison table.
- **Time:** 4 min

#### Slide 4 — Enterprise lens: auditability
- **Key bullets:**
  - Who did what, when, with what inputs
  - Reproducible prompts/contracts
  - Reviewable artifacts (diffs, tests)
- **Speaker notes:** Auditability isn’t bureaucracy; it’s how you scale trust.
- **Visual:** Audit trail diagram.
- **Time:** 3 min

#### Slide 5 — Common failure modes by harness
- **Key bullets:**
  - Chat: hidden context; poor reproducibility
  - IDE: partial context; accidental edits
  - CLI: permission blast radius if misconfigured
  - Cloud: data exposure + connector risks
- **Speaker notes:** Each harness has a different “default risk profile.”
- **Visual:** Risk icons per harness.
- **Time:** 3 min

#### Slide 6 — Why this course prefers CLI later (conceptual)
- **Key bullets:**
  - Clear transcripts
  - Better workflow control surfaces
  - Easier permissioning boundaries
- **Speaker notes:** This is not a product endorsement; it’s about workflow clarity.
- **Visual:** “CLI transcript” document + shield.
- **Time:** 2 min

#### Slide 7 — Common misconceptions (callouts)
- **Key bullets:**
  - Misconception: “IDE assistants are always safer”
  - Reality: safety depends on permissions + review gates
  - Misconception: “Cloud agents are always better”
  - Reality: connectors increase attack surface and data risk
- **Speaker notes:** Choose harnesses based on constraints, not hype.
- **Visual:** Two callout boxes.
- **Time:** 2 min

#### Slide 8 — Takeaway: evaluate harnesses with 5 questions
- **Key bullets:**
  - What context can it access?
  - What tools/actions can it take?
  - What approvals exist?
  - What logs/transcripts exist?
  - How does it handle untrusted input?
- **Speaker notes:** This is a checklist you can use with any vendor/tool.
- **Visual:** “Harness evaluation” checklist.
- **Time:** 2–3 min

### 3) Demo-in-lecture plan (no execution required)
- **Demo moment 1 (Slide 3):** Harness comparison mini-case
  - **Snippet (on-slide):**
    ```text
    Task: "Update a logging format and add tests."
    Chat UI: output plan only (no repo context)
    IDE: suggests edits inline (risk: accidental scope)
    CLI: can read repo + run tests (risk: needs permissions)
    ```
  - **What to point out:** Harness differences change what “good” output looks like.
  - **What could go wrong:** Learners assume tool outputs are comparable without controlling context.

### 4) Examples bank
- **Good example:** “Choose a harness for writing a change plan vs editing code; justify with audit/permissions.”
- **Bad example (why it fails):** “Pick the tool with the biggest model.” (ignores workflow and constraints)
- **Enterprise-safe example:** Default to read-only + transcript logging during early adoption.

### 5) Graphics pack (image/diagram prompts)
- **Grid:** Context access vs tool power
  - Prompt: “A 2x2 matrix: x-axis Tool Power (low→high), y-axis Context Access (low→high); place Chat/IDE/CLI/Cloud in cells.”
  - Nano Banana variant: “Minimal 2x2 quadrant chart with labels and 4 items.”
  - Label: infographic
  - Placement: Slide 2
- **Table graphic:** Harness comparison
  - Prompt: “A comparison table for Chat, IDE, CLI, Cloud with rows: Context sources, Actions, Approvals, Audit logs, Typical risks.”
  - Nano Banana variant: “Minimal table infographic with icons per row.”
  - Label: infographic
  - Placement: Slide 3

### 6) Safety & risk callouts
- **Relevant risks:** Excess permissions; lack of auditability; connector exposure; unsafe defaults.
- **Mitigations to mention:** Least privilege; explicit approvals; transcripts; isolation of untrusted inputs.
- **Critical safety concepts:** Evaluate tools by permissions + audit, not just capability.

