# Sessions 15–16 — Slide Outlines (Fundamentals)

## Session 15 — Tool calling

### 1) Session summary
- **Title:** Tool calling: when the model can invoke actions (and why that changes everything)
- **Purpose (1 sentence):** Explain tool calling as structured function invocation and connect it to capability, reliability, and risk.
- **Learning objectives (3):**
  1. Describe tool calling as structured requests to external tools (via a harness).
  2. Explain how tools expand capability (read data, run tests) while increasing risk (actions).
  3. Identify guardrails: least privilege, allowlists, approvals, output validation.
- **If learners only remember 1 thing:** **Tools turn text errors into real-world errors—permissioning is the safety boundary.**

### 2) Slide-by-slide outline

#### Slide 1 — From “text only” to “act”
- **Key bullets:**
  - Text-only: output is advisory
  - Tool calling: output can trigger actions
  - The harness is the mediator
- **Speaker notes:** Tool calling is the step-change from assistant to agent.
- **Visual:** Two modes diagram (Text-only vs Tool-enabled).
- **Time:** 3 min

#### Slide 2 — What “tool calling” is (conceptual)
- **Key bullets:**
  - Model proposes a tool + arguments
  - Harness validates and executes (or blocks)
  - Results come back as observations
- **Speaker notes:** The model doesn’t “directly” run tools; the harness decides.
- **Visual:** Plan → Tool call → Result loop.
- **Time:** 3 min

#### Slide 3 — Capability expansion (why it helps)
- **Key bullets:**
  - Access to ground truth (repo, tests, docs)
  - Fewer hallucinations (evidence from tools)
  - Faster iteration on real artifacts
- **Speaker notes:** Tools can reduce hallucination by supplying evidence.
- **Visual:** “Evidence” arrows from tools into model output.
- **Time:** 3 min

#### Slide 4 — Risk expansion (why it’s dangerous)
- **Key bullets:**
  - Write actions change state
  - Execution actions can cause outages
  - Connectors increase attack surface
- **Speaker notes:** The blast radius grows with tool power.
- **Visual:** Blast radius rings around tools (read < write < deploy).
- **Time:** 3 min

#### Slide 5 — Tool calling vs “shelling out” vs manual copy/paste
- **Key bullets:**
  - Tool calling: structured, auditable, enforceable
  - Shelling out: flexible but risky without gating
  - Manual: slow, but human-in-the-loop by default
- **Speaker notes:** Structure is what makes governance possible.
- **Visual:** Comparison table.
- **Time:** 3 min

#### Slide 6 — Guardrails (the non-negotiables)
- **Key bullets:**
  - Least privilege permissions
  - Allowlists and scoped tool surfaces
  - Human approvals for write/deploy
  - Validate outputs and tool results
- **Speaker notes:** These guardrails are what make tool calling enterprise-viable.
- **Visual:** Guardrails checklist with shield icons.
- **Time:** 3 min

#### Slide 7 — Common misconceptions (callouts)
- **Key bullets:**
  - Misconception: “Tools make outputs correct”
  - Reality: tools provide evidence, but interpretation can still be wrong
  - Misconception: “If the model can call tools, it should”
  - Reality: choose the minimum tool needed; avoid unnecessary actions
- **Speaker notes:** Tool use should be intentional and justified.
- **Visual:** Two callout boxes.
- **Time:** 2 min

#### Slide 8 — Takeaway: treat tools like production APIs
- **Key bullets:**
  - Threat model them
  - Scope them
  - Log them
  - Approve high-risk calls
- **Speaker notes:** If you wouldn’t expose an API to the internet, don’t expose it to an unconstrained agent.
- **Visual:** “Tool = API” equivalence diagram.
- **Time:** 2 min

### 3) Demo-in-lecture plan (no execution required)
- **Demo moment 1 (Slide 2):** Toy tool-call JSON
  - **Snippet (on-slide):**
    ```json
    {
      "tool": "run_tests",
      "args": {"scope": "unit", "target": "ClaimsEligibility.Tests"}
    }
    ```
  - **What to point out:** Structured arguments enable allowlisting and policy enforcement.
  - **What could go wrong:** Over-broad tools (e.g., “run_any_command”) defeat governance.
- **Demo moment 2 (Slide 6):** Permission ladder
  - **Snippet (on-slide):**
    ```text
    Allowed: read_repo, run_tests
    Requires approval: write_repo
    Prohibited: deploy_prod
    ```
  - **What to point out:** Default-deny for high-blast-radius tools.
  - **What could go wrong:** “Temporary” broad permissions become permanent.

### 4) Examples bank
- **Good example:** “Allow read_repo + run_tests; block write until plan is approved.”
- **Bad example (why it fails):** “Give the agent deploy so it can finish.” (unacceptable blast radius)
- **Enterprise-safe example:** Read-only agent that produces diffs and test plans; humans execute changes.

### 5) Graphics pack (image/diagram prompts)
- **Flowchart:** Tool calling loop
  - Prompt: “A flowchart: Model proposes tool call → Harness validates → Tool executes → Result returned → Model updates plan.”
  - Nano Banana variant: “Minimal loop flowchart with 4 boxes and arrows; include a shield on ‘validate’.”
  - Label: flowchart
  - Placement: Slide 2
- **Infographic:** Blast radius rings
  - Prompt: “Concentric circles labeled Read, Write, Execute, Deploy showing increasing blast radius; enterprise minimal style.”
  - Nano Banana variant: “Minimal concentric circles with labels and small icons.”
  - Label: infographic
  - Placement: Slide 4

### 6) Safety & risk callouts
- **Relevant risks:** Unauthorized actions; insecure connectors; tool misuse; prompt injection driving tool calls.
- **Mitigations to mention:** Least privilege; approvals; allowlists; isolate untrusted inputs; logs/transcripts.
- **Critical safety concepts:** Tool permissioning is a primary safety boundary (expanded in Session 17).

---

## Session 16 — MCP vs API calls

### 1) Session summary
- **Title:** MCP-style protocols vs direct API calls: when standardization helps
- **Purpose (1 sentence):** Explain why a standardized tool protocol can help interoperability and governance, and when it’s unnecessary complexity.
- **Learning objectives (3):**
  1. Contrast direct API calls (point-to-point) with an MCP-style approach (standard protocol for tools).
  2. Identify when MCP-like standardization is justified (multiple tools/clients, consistent patterns, governance).
  3. Identify costs: complexity, operational overhead, security surface.
- **If learners only remember 1 thing:** **Use protocols when you need interoperability and governance—not because it’s trendy.**

### 2) Slide-by-slide outline

#### Slide 1 — The integration spectrum
- **Key bullets:**
  - Simple: direct API calls
  - Moderate: shared tool wrappers
  - Complex: standardized protocol across tools/clients
- **Speaker notes:** You don’t start with maximum architecture.
- **Visual:** Spectrum ladder.
- **Time:** 3 min

#### Slide 2 — Direct API calls (point-to-point)
- **Key bullets:**
  - Fast to implement
  - Tight coupling to one tool/client
  - Governance is ad hoc unless you build it
- **Speaker notes:** Direct is great until you have multiple tool surfaces to manage.
- **Visual:** Single arrow between client and tool.
- **Time:** 3 min

#### Slide 3 — MCP-style approach (conceptual)
- **Key bullets:**
  - Standard interface for tools
  - Consistent invocation and responses
  - Enables common policy enforcement
- **Speaker notes:** Think “USB for tools”: standard plug, many devices.
- **Visual:** Hub-and-spoke diagram with protocol in the middle.
- **Time:** 4 min

#### Slide 4 — When MCP-style is justified
- **Key bullets:**
  - Multiple environments/clients
  - Multiple tool providers
  - Need consistent logging, permissions, and schemas
- **Speaker notes:** Standardization pays off when complexity is already present.
- **Visual:** Decision checklist.
- **Time:** 3 min

#### Slide 5 — When it’s overkill
- **Key bullets:**
  - One client, one tool, simple actions
  - Team lacks operational bandwidth
  - Security surface would expand without benefit
- **Speaker notes:** Over-architecture slows delivery and can add risk.
- **Visual:** “Overkill” warning box.
- **Time:** 3 min

#### Slide 6 — Security and governance considerations
- **Key bullets:**
  - Protocols can centralize policy (good)
  - They also centralize blast radius (risk)
  - You still need least privilege + approvals
- **Speaker notes:** Centralization is not automatically safety; it’s leverage.
- **Visual:** Central policy gate with shield + risk arrow.
- **Time:** 3 min

#### Slide 7 — Common misconceptions (callouts)
- **Key bullets:**
  - Misconception: “Protocols make tools safe”
  - Reality: safety requires permissioning and isolation
  - Misconception: “Direct API calls can’t be governed”
  - Reality: you can govern direct calls; it’s just harder to standardize
- **Speaker notes:** Governance is a design choice regardless of architecture.
- **Visual:** Two callout boxes.
- **Time:** 2 min

#### Slide 8 — Takeaway: choose the simplest path that meets governance
- **Key bullets:**
  - Start direct; add wrappers
  - Introduce a protocol when interoperability becomes a real need
  - Keep security review involved early
- **Speaker notes:** Architecture should follow constraints and scale, not vice versa.
- **Visual:** “Start simple → standardize later” arrow.
- **Time:** 2 min

### 3) Demo-in-lecture plan (no execution required)
- **Demo moment 1 (Slide 3–4):** “Same tool call” across two clients (conceptual)
  - **Snippet (on-slide):**
    ```text
    Client A calls: tool.read_repo(path)
    Client B calls: tool.read_repo(path)
    Standard protocol: same request/response shape, same logs, same policies
    ```
  - **What to point out:** Standard shapes enable shared governance and tooling.
  - **What could go wrong:** Teams adopt protocol but skip policy enforcement; complexity without safety.

### 4) Examples bank
- **Good example:** “You have 5 internal tools and 3 teams; standardize tool schemas and logging.”
- **Bad example (why it fails):** “Use MCP for a single script.” (overhead outweighs benefit)
- **Enterprise-safe example:** Pilot with read-only tools first; add actions only after governance is proven.

### 5) Graphics pack (image/diagram prompts)
- **Diagram:** Hub-and-spoke protocol
  - Prompt: “A hub-and-spoke diagram: clients on left, tools on right, protocol hub in middle; show consistent schemas and logging.”
  - Nano Banana variant: “Minimal hub diagram with labeled nodes: Clients, Protocol, Tools; add shield icon on protocol.”
  - Label: flowchart
  - Placement: Slide 3
- **Checklist:** When to standardize
  - Prompt: “A checklist titled ‘When to Standardize (MCP-style)’ with 5 items; clean enterprise style.”
  - Nano Banana variant: “Minimal checklist card with 5 bullets and icons.”
  - Label: infographic
  - Placement: Slide 4

### 6) Safety & risk callouts
- **Relevant risks:** Expanded integration surface; centralized blast radius; inconsistent tool schemas causing unsafe calls.
- **Mitigations to mention:** Central policy enforcement; least privilege; approvals; audit logs; phased rollout.
- **Critical safety concepts:** Governance still required regardless of architecture choice.

