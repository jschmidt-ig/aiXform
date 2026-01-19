ChatGPT Folder > s6 - Course Syllabus Blocking > Fundamentals-2Week-Syllabus.md

# AI SDLC — Fundamentals (2 Weeks, Lecture-Only)

A lecture-only fundamentals module that establishes the mental model for LLMs, context, agents/harnesses, tool calling/MCP, and security (tool permissions + prompt injection).

**Format:** 20 sessions (lectures and demonstrations), each **20–30 minutes**.  
**Cadence suggestion:** 2 sessions/day, Mon–Fri for 2 weeks (10 days).  
**Assessment:** end-of-module **lecture-only test** (10–15 min) with **critical safety** pass/fail + a separate learner feedback questionnaire.

---

## Audience
- Software engineers, platform engineers, and technical professionals who will later do labs/applied work using CLI harnesses (Claude Code CLI as the primary agentic harness), API calls (e.g., cURL), and tool-based agent workflows.
- No code execution required during Fundamentals lectures.

> **Tooling note:** The Ensemble pilot uses Claude Code CLI. Future clients restricted to GitHub Copilot may require adapted content (placeholder).

---

## Time commitment
- **Lecture time:** 20 sessions × (20–30 min) = **~6.7–10 hours** (typical target: ~8–9 hours)
- **End test:** ~12 minutes
- **Evaluation questionnaire:** 5–7 minutes

---

## Expected outcomes (what a learner should be able to do after Fundamentals)
By the end, learners should be able to:
1) Explain what an LLM is doing at inference time (tokens, prediction framing) and what it is *not* doing (no in-session learning, no durable memory).
2) Explain training vs inference at a high level and why “crystallized intelligence” matters for how you use models.
3) Understand context windows and how context assembly affects quality and safety.
4) Distinguish: chatbot UI vs raw API usage vs agentic harnesses (IDE vs CLI vs cloud agent).
5) Explain what “agentic workflow” means (agentic loop) and where it breaks in practice.
6) Understand tool calling and when it changes capability.
7) Explain MCP at a conceptual level and when it’s justified vs direct API calls.
8) Apply safe judgment on:
   - tool permissioning / least privilege
   - preventing untrusted input from controlling tool calls
   - prompt injection recognition and mitigations

---

## Syllabus at a glance (Day plan: 10 days / 20 sessions)

| Day | Session A (20–30 min) | Session B (20–30 min) |
|---:|---|---|
| 1 | 1) Course orientation | 2) Tooling + constraints |
| 2 | 3) LLMs + tokens | 4) Transformer mental model |
| 3 | 5) Training vs inference + fine-tuning | 6) Context window + no long-term memory |
| 4 | 7) Prompting fundamentals | 8) Chatbot vs raw model call |
| 5 (Fri) | 9) Prompt contracts + output schemas | 10) Context engineering workshop |
| 6 | 11) Agents vs workflows + agentic loop | 12) Harness taxonomy |
| 7 | 13) Agentic coding method | 14) Model-mixing + harness comparisons |
| 8 | 15) Tool calling | 16) MCP vs API calls |
| 9 | 17) Securing tool calls + permissioning | 18) Prompt injection |
| 10 (Fri) | 19) Security lab (lecture-based) | 20) Integrated capstone demo (lecture-based) + recap/Q&A |

---

## Detailed session outlines (what goes into each lecture)

### Day 1
#### Session 1 — Course orientation
- Purpose: what “agentic coding” means in this course (vs “just chatting”)
- What’s coming next (labs/applied later) and why Fundamentals is lecture-only
- Outcomes and the end-of-module safety gate

**Lecture includes**
- “3-layer stack” mental model: (1) model, (2) harness, (3) workflow/governance
- What “good” looks like: smaller safer PRs, better test/docs velocity, less thrash

**Demo ideas (lecture-only)**
- Walk through a simple “task → plan → artifact” without running anything:
  - example: “Write a safe change plan” output contract

#### Session 2 — Tooling + constraints (enterprise reality)
- Constraints: no external SaaS, approved models only, sensitive data classes, security reviews
- Why approvals delay early execution (and how this module avoids that)
- Boundaries: what belongs in prompts/context vs what must never appear

**Key concepts**
- Data classes / redaction mental model
- “Off-network coaching” stance (conceptual)

---

### Day 2
#### Session 3 — LLMs + tokens
- One-sentence definition of inference: next-token prediction given context
- Tokens as units (not words), subword effects, why it matters to cost/limits
- Failure modes that come from token framing (hallucination, overconfidence, format drift)

**Demo ideas**
- Show how the same sentence tokenizes differently (visual screenshot/diagram)
- Show “format drift” examples and why output contracts exist

#### Session 4 — Transformer mental model (no math)
- Embeddings → attention → layers → output distribution (high level)
- Why transformers handle long dependencies *somewhat* but still fail in long contexts
- Intuition for “attention” and why it’s not the same as “reasoning”

**Demo ideas**
- A simple diagram (token stream → attention → output)
- “Where errors come from” slide: missing context vs conflicting instructions

---

### Day 3
#### Session 5 — Training vs inference + fine-tuning (high level)
- Training updates weights; inference uses fixed weights
- “Crystallized intelligence”: capabilities are largely frozen at training time
- Fine-tuning / alignment: what changes (behavior style/policy) vs what doesn’t (core model limits)

**Demo ideas**
- “What you can change” vs “what you can’t” table
- Misconception busting: “it learned from my prompt” (no)

#### Session 6 — Context window + no long-term memory
- Context window mechanics: truncation, recency bias, “lost instructions”
- “Memory” is usually: (a) still in window, (b) re-provided, or (c) external store (in later phases)
- Practical implication: context engineering is a real skill

**Demo ideas**
- Show a long prompt example where early instructions disappear (visual)
- Show a “context packing” pattern (headings, order, brevity)

---

### Day 4
#### Session 7 — Prompting fundamentals
- Prompt anatomy: role, constraints, examples, acceptance criteria, output contract
- Prompt hygiene: clarity, minimal ambiguity, testable outputs
- “Prompt engineering” vs “context engineering” (preview)

**Demo ideas**
- Before/after prompt: vague → structured
- Output contract examples: sections vs JSON schema

#### Session 8 — Chatbot vs raw model call
- What a chatbot UI hides: system/developer messages, safety wrappers, memory features
- Roles/messages mental model: system/dev/user, plus context assembly
- Why API-level thinking matters for agents and harnesses

**Demo ideas**
- “What’s actually sent” diagram: UI → hidden prompts → API
- A sample cURL request *as a slide* (no execution)

---

### Day 5 (Friday)
#### Session 9 — Prompt contracts + output schemas (lecture-only)
- Why contracts matter: grading, automation, reproducibility, safety
- Structured outputs: sections, key-value, JSON schema (conceptual)
- How to validate outputs without running code (checklists)

**Demo ideas**
- 3 example contracts: (a) PR description, (b) risk checklist, (c) change plan

#### Session 10 — Context engineering workshop (lecture-only)
- “Working set” construction: what to include/omit, ordering, compression
- Patterns: summary-first, constraints-first, examples-last; when to invert
- Avoiding “context poisoning”: isolate untrusted content and label it

**Demo ideas**
- 2–3 worked examples of context assembly with explain-why
- “Context budget” slide: what to spend tokens on

---

### Day 6
#### Session 11 — Agents vs workflows + agentic loop
- Agent definition: LLM + tools + loop + objectives
- Agentic loop: plan → act → observe → reflect → iterate
- Where agents fail: mis-specified goals, tool misuse, brittle plans

**Demo ideas**
- “Agent loop” diagram with failure points annotated
- A “safe loop” guardrail checklist (conceptual)

#### Session 12 — Harness taxonomy
- Chatbot vs IDE assistant vs CLI agent vs cloud agent
- What differs: tool surface, context assembly, permissions, auditability
- Why this course is CLI-first (for later phases)

**Demo ideas**
- Harness comparison table: strengths/risks

---

### Day 7
#### Session 13 — Agentic coding method (course focus)
- What "agentic coding" means operationally: plan → diff → test → narrate
- How agentic harnesses differ: Claude Code CLI vs IDE assistants vs browser chat
- The point: workflow design matters more than any single tool

> **Note:** This course uses Claude Code CLI as the primary harness. Concepts apply to other agentic tools (GitHub Copilot CLI, Cursor, etc.) with workflow adaptations.

**Demo ideas**
- A “PR narration” template and why it’s useful
- “Do not let the agent deploy” principle preview

#### Session 14 — Model mixing + harness comparisons
- Why mixing models is feasible (no durable memory)
- When to use “bigger thinking” vs “smaller fast” models (conceptual)
- Trade-offs: cost, latency, reliability, safety

**Demo ideas**
- A “model selection” decision tree (simple)

---

### Day 8
#### Session 15 — Tool calling
- What tool calling is: structured function invocation via the harness
- Why it expands capability (and why it introduces risk)
- Tool calling vs “shelling out” vs “manual copy/paste” (conceptual)

**Demo ideas**
- A toy example: model proposes a tool call JSON vs non-tool model (visual)

#### Session 16 — MCP vs API calls
- API calls: direct point-to-point model invocation
- MCP: standardized tool interoperability + multi-step coordination patterns
- When MCP is justified (vs unnecessary complexity)

**Demo ideas**
- Simple “MCP vs API” table: benefits/risks

---

### Day 9
#### Session 17 — Securing tool calls + permissioning
- Least privilege: allowlists, scopes, approval gates
- Auditability: logs, transcripts, “who did what when”
- Preventing untrusted inputs from driving tool calls (policy)

**Demo ideas**
- Permission sets example: read-only vs read+test vs write vs deploy

#### Session 18 — Prompt injection
- What injection is: untrusted text attempting to override instructions
- Common injection patterns (documents, web pages, repo text)
- Mitigations: input isolation, instruction hierarchy, tool gating, output validation

**Demo ideas**
- “Injection attempt” examples and how to respond (lecture-only)

---

### Day 10 (Friday)
#### Session 19 — Security lab (lecture-based)
- Learners analyze 2–3 scenarios:
  - pick safe permissions
  - identify injection
  - choose mitigations
- Reinforce “critical safety” principles that are hard-fail on the test

#### Session 20 — Integrated capstone demo + recap/Q&A (lecture-based)
- Walk end-to-end conceptually:
  1) raw API call mental model
  2) harness behavior
  3) tool calling capabilities
  4) injection attempt
  5) mitigations + permissioning
- Final recap of what Fundamentals enables in labs/applied

---

## End-of-module test (10–15 minutes)

**Rules**
- 10 questions total (6 comprehension + 4 scenario judgments)
- **Pass:** ≥80% overall (8/10) AND 0 misses on **critical safety** questions
- **Critical safety questions (hard fail if missed):**
  - prompt injection recognition + response
  - least-privilege tool permissioning
  - “untrusted text cannot directly control tool calls” principle

(Include the test handout from the bundle file: `Fundamentals-End-Test.md`.)

---

## Learner evaluation questionnaire (5–7 minutes)
Not pass/fail. Used to improve the course and identify adoption blockers.  
(Include the questionnaire from the bundle file: `Learner-Evaluation-Questionnaire.md`.)
