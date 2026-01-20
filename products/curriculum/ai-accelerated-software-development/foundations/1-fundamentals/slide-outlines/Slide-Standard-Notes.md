# Slide Standard Notes (Fundamentals Slide Outlines)

These notes define the repeatable “house style” for Fundamentals slide outlines so decks feel consistent across all 20 sessions.

## Audience + Delivery Assumptions
- Audience: mid/senior enterprise software engineers.
- Format: **lecture-only** (20–30 minutes per session). Learners do **not** run tools during Fundamentals.
- Tooling: **tool-agnostic** concepts; demos are **on-slide** examples (snippets / transcripts), not live execution.
- Enterprise constraints are always in-scope: approved models only, no external SaaS uploads, PHI/PII sensitivity, security review realities.

## Slide Density + Timing
- Target: **9–11 slides per session**.
- Default pacing: ~2 minutes/slide with **one 3–4 minute “demo-in-lecture” moment**.
- Avoid >5 bullets per slide. Prefer diagrams/tables.

## Required Elements (Per Session)
1) Session summary (purpose, objectives, “remember 1 thing”).
2) Slide-by-slide outline:
   - Slide title
   - Key bullets (≤5)
   - Speaker notes (short; what to say)
   - Visual suggestion (diagram/table)
   - Time estimate
3) Demo-in-lecture plan (1–2 demos; snippets/transcripts only).
4) Examples bank (good / bad / enterprise-safe).
5) Graphics pack (2–4 visuals with prompts + placement).
6) Safety & risk callouts (include “critical safety” flags where relevant).

## Reusable Visual Motifs (Use Often)
- **3-layer stack:** Model → Harness → Workflow/Governance.
- **Agentic loop:** Plan → Act → Observe → Reflect → Iterate (with guardrails).
- **Context budget:** Token “spend” by priority (constraints, examples, artifacts).
- **Permission ladder:** read → test → write → deploy (with approval gates).
- **Instruction hierarchy:** system > developer > user > untrusted content.

## Reusable Demo Snippet Patterns (Lecture-Only)
- “Task → Plan → Artifact” output contract:
  - Plan checklist
  - Risks
  - Patch proposal
  - Test plan
- Prompt contract skeletons (Markdown sections) and structured output “schemas” (conceptual JSON).
- Sanitized context pack example with explicit redaction rules.
- Tool-call JSON examples (toy tools; no real credentials).
- “Injection attempt” snippet + correct refusal / isolation behavior.

## Common Misconception Callouts (1–2 per Session)
Prefer callouts with this structure:
- **Misconception:** …
- **Reality:** …
- **Why it matters:** …

## Safety Framing (Always)
- Never recommend copying sensitive data or whole production codebases into prompts.
- Treat any untrusted text as potentially malicious (prompt injection).
- Emphasize **least privilege** and **approval gates** for any action-like tools.
- When discussing “agents,” explicitly name the failure modes: goal drift, tool misuse, context poisoning, silent data exposure.

