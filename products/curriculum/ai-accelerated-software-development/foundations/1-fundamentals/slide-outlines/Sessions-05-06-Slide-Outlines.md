# Sessions 05–06 — Slide Outlines (Fundamentals)

## Session 5 — Training vs inference + fine-tuning (high level)

### 1) Session summary
- **Title:** What training changes (weights) vs what prompting changes (context)
- **Purpose (1 sentence):** Correct the “it learned from my prompt” misconception and set expectations about customization (fine-tuning, alignment) at a high level.
- **Learning objectives (3):**
  1. Distinguish training (updates weights) from inference (fixed weights).
  2. Explain “crystallized intelligence”: most capability is fixed at training time.
  3. Describe what fine-tuning/alignment can change (style/policy) vs cannot (fundamental limits).
- **If learners only remember 1 thing:** **Prompting changes inputs; training changes the model.**

### 2) Slide-by-slide outline

#### Slide 1 — The core distinction
- **Key bullets:**
  - Training: update weights (slow, expensive)
  - Inference: use fixed weights (fast, repeatable)
  - Most enterprise use is inference + workflow
- **Speaker notes:** Prompting is not training; it’s “programming the input.”
- **Visual:** Two-lane timeline: Train (weights change) vs Infer (context changes).
- **Time:** 3 min

#### Slide 2 — “Crystallized intelligence” (why it matters)
- **Key bullets:**
  - Capabilities are mostly fixed
  - You can steer behavior, not add magic new knowledge
  - Good workflows compensate for limits
- **Speaker notes:** This is why verification and guardrails matter more than “clever prompts.”
- **Visual:** “Fixed capabilities” block + “steering knobs” (context, tools).
- **Time:** 3 min

#### Slide 3 — What fine-tuning is (high level)
- **Key bullets:**
  - Adjusts behavior patterns on curated data
  - Often improves style/format/domain phrasing
  - Doesn’t eliminate hallucinations or guarantee truth
- **Speaker notes:** Fine-tuning can reduce friction, but it’s not a substitute for safety.
- **Visual:** “Base model” → “fine-tuned model” with arrows to “format/style”.
- **Time:** 3 min

#### Slide 4 — Alignment and policy layers (conceptual)
- **Key bullets:**
  - Safety policies constrain outputs/actions
  - Harness layers add additional controls
  - Policies vary across environments
- **Speaker notes:** Don’t assume behaviors are portable across tools.
- **Visual:** Stack: model → policy → harness → workflow.
- **Time:** 2 min

#### Slide 5 — “What you can change” vs “what you can’t”
- **Key bullets:**
  - Can: output format, tone, domain terms, checklists
  - Can’t: context window limits, perfect truth, zero mistakes
  - Must: verify and review
- **Speaker notes:** This table is a sanity check for expectations.
- **Visual:** Two-column table.
- **Time:** 3 min

#### Slide 6 — When prompts feel like learning (but aren’t)
- **Key bullets:**
  - Within-window continuity feels like memory
  - Repetition creates consistency (not learning)
  - External memory is a separate system (later)
- **Speaker notes:** We’ll cover context windows next; this is the bridge.
- **Visual:** “In window” vs “out of window” boundary.
- **Time:** 2 min

#### Slide 7 — Common misconceptions (callouts)
- **Key bullets:**
  - Misconception: “The model learns from each chat”
  - Reality: chats change context, not weights
  - Misconception: “Fine-tuning makes it safe”
  - Reality: safety still needs permissions + review + isolation
- **Speaker notes:** Mis-set expectations cause unsafe reliance.
- **Visual:** Two callout boxes.
- **Time:** 2 min

#### Slide 8 — Practical guidance for teams
- **Key bullets:**
  - Standardize contracts and context packs
  - Measure outcomes (quality, risk, cycle time)
  - Escalate customization only when workflow hits limits
- **Speaker notes:** Most wins come from process change, not model change.
- **Visual:** Maturity ladder: templates → automation → tuned workflows.
- **Time:** 2–3 min

### 3) Demo-in-lecture plan (no execution required)
- **Demo moment 1 (Slide 5):** Table walkthrough with a concrete example
  - **Snippet (on-slide):**
    ```text
    Goal: "Always output a change plan with sections A/B/C"
    Prompting: Works (contract in context)
    Fine-tuning: Might help consistency across many prompts
    Still required: human review + tests
    ```
  - **What to point out:** Structure is easy to steer; correctness still requires verification.
  - **What could go wrong:** Learners assume “format success” implies “logic success.”

### 4) Examples bank
- **Good example:** “Use this output contract to draft a change plan; list assumptions explicitly.”
- **Bad example (why it fails):** “Learn our company policies from this chat and remember them forever.” (category error)
- **Enterprise-safe example:** Put policies into a reusable template doc; re-provide it as needed (sanitized, approved).

### 5) Graphics pack (image/diagram prompts)
- **Diagram:** Train vs inference
  - Prompt: “A split diagram: Training updates weights; Inference uses context; show arrows to outputs.”
  - Nano Banana variant: “Two-lane diagram with headings ‘Training (weights change)’ and ‘Inference (context changes)’.”
  - Label: infographic
  - Placement: Slide 1
- **Table graphic:** What you can change vs can’t
  - Prompt: “A clean table titled ‘What prompting can change vs cannot’; include 5 rows.”
  - Nano Banana variant: “Minimal table infographic with icons (slider vs lock).”
  - Label: infographic
  - Placement: Slide 5

### 6) Safety & risk callouts
- **Relevant risks:** Over-trusting “customized” behavior; treating alignment as a security boundary.
- **Mitigations to mention:** Permissioning + audit logs + approvals; verify outputs; treat policies as workflow artifacts.
- **Critical safety concepts:** Safety is not guaranteed by training/fine-tuning alone.

---

## Session 6 — Context window + no long-term memory

### 1) Session summary
- **Title:** Context windows: truncation, recency bias, and “memory” myths
- **Purpose (1 sentence):** Teach learners to reason about what the model can “see” and how to design around forgetting and truncation.
- **Learning objectives (3):**
  1. Explain what happens when context exceeds the window (truncation/omission).
  2. Describe why “memory” is usually just “still in context” or “re-provided.”
  3. Apply basic context packing patterns (constraints first, summaries, minimal artifacts).
- **If learners only remember 1 thing:** **The model only knows what you put in the window (right now).**

### 2) Slide-by-slide outline

#### Slide 1 — The window is the workspace
- **Key bullets:**
  - Context window = maximum tokens the model processes
  - The model can’t access what isn’t in the window
  - “Memory” is a separate system (later phases)
- **Speaker notes:** Treat context like RAM, not disk.
- **Visual:** “RAM (window)” vs “Disk (external store)” analogy diagram.
- **Time:** 3 min

#### Slide 2 — What truncation looks like
- **Key bullets:**
  - Older content can be dropped
  - Key constraints can disappear
  - Outputs change without obvious reason
- **Speaker notes:** This is why “it was working yesterday” happens.
- **Visual:** Long prompt with faded/struck early instructions.
- **Time:** 3 min

#### Slide 3 — Recency + salience effects (practical)
- **Key bullets:**
  - Recent instructions often dominate
  - Highly specific text can “pull attention”
  - Contradictions amplify instability
- **Speaker notes:** You design for this by ordering and labeling content.
- **Visual:** “Priority ordering” ladder.
- **Time:** 2–3 min

#### Slide 4 — Context packing: what to include
- **Key bullets:**
  - Constraints + acceptance criteria
  - Minimal relevant artifacts (interfaces, error shapes)
  - Examples (good/bad) to steer output
- **Speaker notes:** The best context is curated, not maximal.
- **Visual:** Context pack checklist.
- **Time:** 3 min

#### Slide 5 — Context packing: what to exclude
- **Key bullets:**
  - Whole repos; large dumps; irrelevant history
  - Untrusted raw documents (unless isolated)
  - Sensitive data (policy)
- **Speaker notes:** Overfeeding causes forgetting of what matters most.
- **Visual:** “Do not include” stop-list.
- **Time:** 2 min

#### Slide 6 — Compression patterns (summary-first)
- **Key bullets:**
  - Start with a short summary and constraints
  - Put details later
  - Add a “context budget” limit line
- **Speaker notes:** Summaries are “anchors” that survive even when details shift.
- **Visual:** Example: summary block at top of a prompt.
- **Time:** 3 min

#### Slide 7 — “Memory” myths (callouts)
- **Key bullets:**
  - Misconception: “It remembers my preference forever”
  - Reality: it repeats patterns in-window; otherwise you must re-provide
  - Misconception: “If I say it once, it will follow”
  - Reality: instructions can be displaced or contradicted
- **Speaker notes:** The workflow must re-assert constraints.
- **Visual:** Two callout boxes.
- **Time:** 2 min

#### Slide 8 — Practical takeaway: design a reusable context pack
- **Key bullets:**
  - A 1-page system summary (sanitized)
  - A contract library (outputs)
  - A redaction policy snippet
- **Speaker notes:** This is the start of “context engineering” as a team practice.
- **Visual:** “Reusable pack” folder icon with 3 docs.
- **Time:** 2 min

### 3) Demo-in-lecture plan (no execution required)
- **Demo moment 1 (Slide 2 or 6):** “Lost constraint” scenario
  - **Snippet (on-slide):**
    ```text
    Early instruction: "Do NOT change database schema."
    40 messages later: instruction no longer present.
    Output: proposes adding a column.
    Fix: re-state constraints at top of each request.
    ```
  - **What to point out:** Constraints should be repeated and placed early; don’t rely on long chat history.
  - **What could go wrong:** Learners blame the model instead of the context assembly.

### 4) Examples bank
- **Good example:** “Here’s a 12-line context pack; propose a plan; restate constraints.”
- **Bad example (why it fails):** “Here are 50 pages of logs.” (forces truncation; hides constraints)
- **Enterprise-safe example:** Summarize logs into error shapes + counts; redact identifiers; link to internal systems instead of pasting.

### 5) Graphics pack (image/diagram prompts)
- **Diagram:** Context window as RAM
  - Prompt: “A simple analogy diagram: ‘Context window (RAM)’ vs ‘External memory (Disk)’; include icons.”
  - Nano Banana variant: “Minimal two-box diagram labeled RAM and Disk, with arrows showing re-providing context.”
  - Label: infographic
  - Placement: Slide 1
- **Infographic:** Context pack checklist
  - Prompt: “A checklist card titled ‘Context Pack’ with 6 items; clean enterprise design.”
  - Nano Banana variant: “Checklist infographic with check icons and short labels.”
  - Label: infographic
  - Placement: Slide 4

### 6) Safety & risk callouts
- **Relevant risks:** Hidden truncation causing unsafe outputs; untrusted content buried in long context; accidental data exposure.
- **Mitigations to mention:** Summary-first; constraints-first; isolate untrusted inputs; keep context small and approved.
- **Critical safety concepts:** Reinforces “constraints must be explicit and repeated.”

