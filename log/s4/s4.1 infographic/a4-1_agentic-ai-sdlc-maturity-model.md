# Agentic AI SDLC Maturity Model (Mental Models + Scope + Controls)

This document captures a practical progression model for using AI coding tools—from “autocomplete” to managing a hierarchical team of agents—centered on two things:
1) the **software engineer’s mental model** (“what am I doing?”), and  
2) the **assistant/agent’s mental model** (“what is the AI doing?”).

It’s designed to be used for enablement, coaching, or as a shared vocabulary inside an engineering org.

---

## The two-axis idea: **Depth** and **Breadth** (it’s not purely linear)

As you move up the maturity curve, growth is not just “more autonomy.” It expands in two directions:

- **Depth (capability / seniority):** the agent(s) can perform more senior engineering work—architecture thinking, design trade-offs, testing strategy, risk management, etc.
- **Breadth (scope / unit of work):** the unit of delegation grows from **snippets** → **tickets/stories** → **features** → **milestones**.

A good infographic shows both axes, with levels roughly tracing a diagonal from low-depth/low-breadth to high-depth/high-breadth.

---

## Level overview (5 levels)

### Level 1 — Autocomplete Assist (Copilot mode)
- **Engineer mental model:** *“I’m driving. AI is a turbocharged autocomplete.”*
- **AI mental model:** *“Predict the next token / line given local context.”*
- **Unit of work:** snippets, lines, small functions
- **Control loop:** human writes; AI suggests; human accepts/rejects

**Naming options:** Autocomplete Assist / Inline Copilot / Suggestion Mode

---

### Level 2 — Supervised Agent Coding (Junior dev on your shoulder)
- **Engineer mental model:** *“I’m pairing with a junior dev. I stay in the loop and approve tool usage.”*
- **AI mental model:** *“I can propose edits and run tools, but I’m supervised step-by-step.”*
- **Unit of work:** files, small refactors, discrete tasks inside a story
- **Control loop:** human approves actions; reviews most code; commits under their account

**Naming options:** Supervised Agent / Pair-Programming Agent / “Shoulder Surf” Mode

---

### Level 3 — PR-Submitting Agent (End-to-end story delivery)
- **Engineer mental model:** *“I delegate a story and review the PR.”*
- **AI mental model:** *“I can complete a user story end-to-end and open a PR for review.”*
- **Unit of work:** a full story (ticket) with acceptance criteria
- **Control loop:** human reviews PR; merges; still can deep-review code, but time is spent more on intent, risk, and tests

**Naming options:** PR Agent / Delegate-to-PR / Story Owner Agent

---

### Level 4 — Multi-Agent Orchestration (Specialists + parallelism; features/milestones)
- **Engineer mental model:** *“I run a small ‘agent team’ (architect, UI, testing, docs) and orchestrate them.”*
- **AI mental model:** *“Multiple specialized agents collaborate; I coordinate plans and integrate outputs.”*
- **Unit of work:** features and (sometimes) milestones
- **Control loop:** more **spot-checking** than line-by-line review; rely more on **test/CI signals** and functional verification

**Naming options:** Orchestrator Mode / Specialist Agents / Parallel Agents

---

### Level 5 — Agent Org / Hierarchical Team (roles, workflows, evals)
- **Engineer mental model:** *“I’m managing an AI ‘org’: roles, responsibilities, governance, and evaluation.”*
- **AI mental model:** *“A hierarchy of agents executes workflows with decision gates and ongoing evaluation.”*
- **Unit of work:** milestones, epics, programs
- **Control loop:** governance + evals + monitoring; human focuses on outcomes, risk, and strategic direction

**Naming options:** Agent Organization / Managed Autonomy / AI Delivery Org

---

## What changes at each level (the “big levers”)

### 1) The human role shifts
- Level 1: **Author**
- Level 2: **Pair + Supervisor**
- Level 3: **Reviewer + Approver**
- Level 4: **Lead + Integrator**
- Level 5: **Manager + Governor**

### 2) The AI role shifts
- Level 1: **Completer**
- Level 2: **Implementer (supervised)**
- Level 3: **Implementer (delegated) + PR author**
- Level 4: **Specialists (parallel) + integrators**
- Level 5: **Org chart with decision-making + eval loops**

### 3) The quality signal shifts
- Level 1–2: correctness is primarily ensured by **human inspection**
- Level 3: correctness shifts toward **PR review + tests**
- Level 4–5: correctness shifts toward **higher-level signals**:
  - unit/integration tests
  - CI gates
  - functional checks
  - eval harnesses and monitoring (Level 5)

This aligns with an enablement approach that emphasizes prompt hygiene, safe PR practices, and rubric-based review and testing signals. fileciteturn2file2L12-L21

---

## Advanced capabilities: where to “slot” them

These capabilities are often discussed as separate “features,” but they naturally map into the maturity curve:

### Model routing / different reasoning levels
- **Appears around:** Level 3+
- **Why:** once you’re delegating whole stories and beyond, you start choosing models by task:
  - light/fast model for refactors and boilerplate
  - strong reasoning model for architecture, tricky bugs, complex tests
- **Visual:** add a “Model Router” badge on Levels 3–5

### “Council of Experts” / ensemble of models
- **Appears around:** Level 4–5
- **Why:** multi-agent coordination benefits from disagreement + cross-checking
- **Visual:** badge: “Council of Experts” on Levels 4–5

### Knowledge graph / RAG / project memory
- **Appears around:** Level 4–5
- **Why:** bigger units of work require persistent context (decisions, architecture, standards)
- **Visual:** badge: “Project Memory / RAG” on Levels 4–5

### Voice agent for management / ops
- **Appears around:** Level 5 (sometimes late Level 4)
- **Why:** when you’re orchestrating many agents, voice can be a control plane
- **Visual:** badge: “Voice Ops” on Level 5

### Evals (automated evaluation / scoring)
- **Appears around:** Level 5
- **Why:** governance and quality need consistent, repeatable evaluation
- **Visual:** badge: “Evals + Monitoring” on Level 5

---

## Productivity: a *heuristic* curve (not a promise)

It’s useful to show an indicative productivity curve—but it should be framed as a **wide range** that depends on:
- domain complexity
- test maturity
- CI speed
- tool friction / security constraints
- clarity of tickets and acceptance criteria

**Suggested “range-style” visualization:** show *multipliers* as bands, not a single number.

Example **heuristic bands** (very rough, for visualization):
- **L1 (Autocomplete):** ~1.05× – 1.3×  
- **L2 (Supervised agent):** ~1.2× – 2×  
- **L3 (PR agent):** ~1.5× – 4×  
- **L4 (Multi-agent):** ~2× – 8×  
- **L5 (Agent org):** ~3× – 15×  

To make this defensible, pair it with measurable engineering KPIs like **cycle time, PR throughput, test coverage, docs completeness, adoption, developer satisfaction**. fileciteturn2file15L7-L18



---

## Naming guidance (so it lands well in enterprise)
If you want names that sound more “professional than belts,” lean into role/progression language—this matches common enterprise naming patterns. fileciteturn2file6L13-L21

A clean naming set:
1. **Assist**
2. **Pair**
3. **Delegate**
4. **Orchestrate**
5. **Govern**

Alternative set (more technical):
1. **Copilot**
2. **Supervised Agent**
3. **PR Agent**
4. **Multi-Agent Orchestrator**
5. **Agent Org**

---

## Appendix: Guardrails checklist by level (quick)

- **L1–2:** prompt hygiene; safe data handling; humans review most changes.
- **L3:** PR templates; acceptance criteria; tests required; PR narration (“what/why/how tested”).
- **L4:** enforce CI gates; functional checks; use spot-check strategy on critical code.
- **L5:** eval harness; policy + workflow; audit trails; periodic reviews; clear role permissions.

For a curriculum lens, this maps cleanly to building prompt hygiene and safe PR strategy early, then scaling into brownfield analysis, gates, and capstones over a 10-week arc. fileciteturn2file9L23-L35
