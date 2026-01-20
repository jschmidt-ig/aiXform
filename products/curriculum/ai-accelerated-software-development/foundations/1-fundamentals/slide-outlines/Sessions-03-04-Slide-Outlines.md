# Sessions 03–04 — Slide Outlines (Fundamentals)

## Session 3 — LLMs + tokens

### 1) Session summary
- **Title:** LLM inference: tokens, prediction framing, and why outputs drift
- **Purpose (1 sentence):** Give learners the simplest accurate mental model for what the model is doing so they can predict failure modes.
- **Learning objectives (3):**
  1. Define inference as next-token prediction given context (and what it is not).
  2. Explain what tokens are (subwords) and why tokenization affects cost/limits.
  3. Identify common failure modes from “token framing” (hallucination, overconfidence, format drift).
- **If learners only remember 1 thing:** **The model predicts tokens; reliability comes from constraints + verification, not vibes.**

### 2) Slide-by-slide outline

#### Slide 1 — The one-sentence model of an LLM
- **Key bullets:**
  - Inference = next-token prediction given context
  - No built-in truth checking
  - Output is a *plausible continuation*, not a database lookup
- **Speaker notes:** If you remember nothing else: it predicts tokens; everything else is harness/workflow.
- **Visual:** Single-line definition in a box + “NOT: search / DB / reasoning engine” icons.
- **Time:** 3 min

#### Slide 2 — Tokens: what they are (and aren’t)
- **Key bullets:**
  - Tokens are model units (often subwords)
  - Different models tokenize differently
  - Code and identifiers can tokenize “expensively”
- **Speaker notes:** Token count is the true “budget” for context and cost.
- **Visual:** Word → tokens segmentation example (simple).
- **Time:** 3 min

#### Slide 3 — Why tokenization matters in practice
- **Key bullets:**
  - Cost scales with input + output tokens
  - Long contexts risk truncation (covered later)
  - Dense prompts reduce room for examples/tests
- **Speaker notes:** Token budgets are like bandwidth; you choose what to send.
- **Visual:** “Context budget” bar (Constraints / Artifacts / Examples / Slack).
- **Time:** 2 min

#### Slide 4 — Probabilities, not certainty
- **Key bullets:**
  - The model samples from a distribution
  - High confidence tone ≠ correctness
  - Small prompt changes can shift outputs
- **Speaker notes:** Treat outputs as drafts; the workflow makes them reliable.
- **Visual:** Output distribution curve with “top candidates”.
- **Time:** 2 min

#### Slide 5 — Failure mode: hallucination (why it happens)
- **Key bullets:**
  - Missing context → “fill in the blanks”
  - Conflicting context → compromise output
  - Ambiguous task → broad assumptions
- **Speaker notes:** Hallucination is often a *context problem*.
- **Visual:** 3-box causal diagram (missing/conflicting/ambiguous → errors).
- **Time:** 3 min

#### Slide 6 — Failure mode: format drift
- **Key bullets:**
  - Without a contract, output structure wanders
  - “Looks right” can still be unusable
  - Contracts turn prose into testable artifacts
- **Speaker notes:** The fix isn’t “ask again”; it’s “specify format + validate”.
- **Visual:** Before/after output (freeform vs structured sections).
- **Time:** 3 min

#### Slide 7 — Contracts preview (why we’ll use them constantly)
- **Key bullets:**
  - Contracts support grading, automation, and safety checks
  - They reduce ambiguity and scope creep
  - They enable “review like code”
- **Speaker notes:** A contract is a pre-commit on what “done” looks like.
- **Visual:** Contract template card (What/Why/Risks/Tests).
- **Time:** 2 min

#### Slide 8 — Common misconceptions (callouts)
- **Key bullets:**
  - Misconception: “Tokens = words”
  - Reality: tokens are subword units; cost/limits follow tokens
  - Misconception: “If it answered confidently, it’s true”
  - Reality: confidence tone is not calibrated truth
- **Speaker notes:** These misconceptions drive unsafe usage patterns.
- **Visual:** Two callout boxes.
- **Time:** 2 min

#### Slide 9 — Takeaway: how to get reliable value
- **Key bullets:**
  - Provide the right context (later: context engineering)
  - Use explicit output contracts
  - Verify with tests/checklists/human review
- **Speaker notes:** Reliability is engineered; it’s not a property of “better prompting” alone.
- **Visual:** “Context → Contract → Verify” triangle.
- **Time:** 2 min

### 3) Demo-in-lecture plan (no execution required)
- **Demo moment 1 (Slide 2):** Tokenization intuition (toy example)
  - **Snippet (on-slide):**
    ```text
    "authorization"  ->  auth | or | ization   (example)
    "AuthZHeaderV2"  ->  Auth | Z | Header | V | 2
    ```
  - **What to point out:** Identifiers and code-like text can explode token count; different models split differently.
  - **What could go wrong:** Learners assume “short prompt” by words but hit context/cost limits by tokens.
- **Demo moment 2 (Slide 6):** Format drift vs contract
  - **Snippet (on-slide):**
    ```text
    OUTPUT CONTRACT:
    1) Assumptions
    2) Proposed change (≤3 steps)
    3) Risks (≥2)
    4) Tests (unit/integration)
    ```
  - **What to point out:** Contracts make outputs checkable and repeatable across runs/tools.
  - **What could go wrong:** Overly rigid schemas when the task is exploratory (use sections first, strict JSON later).

### 4) Examples bank
- **Good example:** “Given these constraints and an output contract, draft a change plan for adding correlation IDs.”
- **Bad example (why it fails):** “Tell me everything about our system and fix it.” (no context, no boundaries, invites hallucination)
- **Enterprise-safe example:** Use synthetic interfaces + redacted error shapes; request hypotheses + tests, not “the answer”.

### 5) Graphics pack (image/diagram prompts)
- **Diagram:** Next-token prediction framing
  - Prompt: “A simple diagram showing context tokens flowing into a model and producing the next token; minimal style.”
  - Nano Banana variant: “Flow diagram: ‘Context (tokens)’ → ‘LLM’ → ‘Next token distribution’ → ‘Sampled output’.”
  - Label: flowchart
  - Placement: Slide 1 or 4
- **Infographic:** Context budget bar
  - Prompt: “A horizontal bar chart labeled ‘Context budget’ divided into: Constraints, Artifacts, Examples, Slack.”
  - Nano Banana variant: “Minimal bar infographic with 4 labeled segments; enterprise palette.”
  - Label: infographic
  - Placement: Slide 3

### 6) Safety & risk callouts
- **Relevant risks:** Over-trusting plausible text; missing context causing confident wrong answers; format drift hiding mistakes.
- **Mitigations to mention:** Output contracts; verification checklists; “assumptions first” sections.
- **Critical safety concepts:** None new; sets up later safety gates.

---

## Session 4 — Transformer mental model (no math)

### 1) Session summary
- **Title:** Transformer intuition: embeddings + attention + layers (high-level)
- **Purpose (1 sentence):** Provide a “good-enough” internal picture of how transformers process context so learners understand limitations and design better prompts/context.
- **Learning objectives (3):**
  1. Describe the pipeline: tokenization → embeddings → attention across tokens → layered transformation → output distribution.
  2. Explain why “attention” is not the same as “reasoning” (and why long context still fails).
  3. Connect model limitations to practical tactics: provide missing context, reduce conflicts, constrain outputs.
- **If learners only remember 1 thing:** **Transformers “attend” to context patterns; they don’t guarantee truth or deep understanding.**

### 2) Slide-by-slide outline

#### Slide 1 — What a transformer gives you (intuition)
- **Key bullets:**
  - A way to use *all* tokens to predict the next token
  - Strong pattern completion across languages and code
  - Still brittle under missing/conflicting context
- **Speaker notes:** This is why it feels smart—and why it can fail in surprising ways.
- **Visual:** Token stream → “attention” highlight → output token.
- **Time:** 2–3 min

#### Slide 2 — Tokenization → embeddings (what “meaning” starts as)
- **Key bullets:**
  - Tokens become vectors (embeddings)
  - Similar tokens often map near each other
  - Code identifiers are “just tokens” too
- **Speaker notes:** Embeddings are a geometry trick: similar patterns cluster.
- **Visual:** Simple 2D embedding scatter (conceptual, not literal).
- **Time:** 3 min

#### Slide 3 — Attention (the useful intuition)
- **Key bullets:**
  - Each token can “look at” other tokens
  - Helps track relationships (e.g., variable use)
  - Attention weights shift based on context
- **Speaker notes:** Attention is a mechanism for relevance, not a proof of reasoning.
- **Visual:** Attention matrix heatmap (toy).
- **Time:** 3 min

#### Slide 4 — Layers (why it can compose patterns)
- **Key bullets:**
  - Multiple layers build higher-level features
  - Later layers refine predictions
  - Still: no guarantee of correctness
- **Speaker notes:** Think “pattern refinement,” not “symbolic logic.”
- **Visual:** Stacked layers with arrows.
- **Time:** 2 min

#### Slide 5 — Why long contexts still fail
- **Key bullets:**
  - Context windows are finite
  - Recency and salience effects
  - Conflicts cause unstable outputs
- **Speaker notes:** More context is not always better; *better curated* context wins.
- **Visual:** Long prompt with faded early instructions.
- **Time:** 3 min

#### Slide 6 — The “missing vs conflicting context” diagnosis
- **Key bullets:**
  - Missing: model invents plausible details
  - Conflicting: model merges or chooses randomly
  - Fix: add constraints, remove contradictions
- **Speaker notes:** This becomes your debugging tool for AI outputs.
- **Visual:** Two-column diagnosis table.
- **Time:** 3 min

#### Slide 7 — Practical implications for engineers
- **Key bullets:**
  - Provide key interfaces + constraints (not everything)
  - Use contracts to keep outputs stable
  - Ask for assumptions + uncertainty explicitly
- **Speaker notes:** “Explain assumptions” is a safety feature.
- **Visual:** “Context → Contract → Verify” loop.
- **Time:** 2 min

#### Slide 8 — Common misconceptions (callouts)
- **Key bullets:**
  - Misconception: “Attention = reasoning”
  - Reality: attention is relevance weighting; reasoning quality varies
  - Misconception: “Add more context to fix everything”
  - Reality: uncurated context can poison outputs
- **Speaker notes:** We’ll formalize context engineering later.
- **Visual:** Two callout boxes.
- **Time:** 2 min

#### Slide 9 — Takeaway: teach the model what matters
- **Key bullets:**
  - Highlight constraints and acceptance criteria
  - Remove conflicting instructions
  - Keep a clean “working set”
- **Speaker notes:** Don’t feed the model a haystack and hope it finds the needle.
- **Visual:** “Working set” box with labeled sections.
- **Time:** 2 min

### 3) Demo-in-lecture plan (no execution required)
- **Demo moment 1 (Slide 6):** Diagnose an answer failure
  - **Snippet (on-slide):**
    ```text
    Prompt: "Fix the timeout bug in Service A."
    Context: (1) says "do not change retries", (2) says "increase retries".
    Output: inconsistent plan + contradictory steps.
    ```
  - **What to point out:** Contradictions produce unstable plans; resolve conflicts before asking for a plan.
  - **What could go wrong:** Learners “argue with the model” instead of fixing context quality.

### 4) Examples bank
- **Good example:** “Here’s the interface + constraints + a failing test description. Propose 2–3 hypotheses and tests.”
- **Bad example (why it fails):** “Read our entire repo and tell us the bug.” (unbounded context; invites hallucinations)
- **Enterprise-safe example:** Provide redacted stack traces and a minimal reproduction description (no PHI/PII).

### 5) Graphics pack (image/diagram prompts)
- **Diagram:** Token stream → attention → output
  - Prompt: “A simple transformer pipeline diagram: tokens → embeddings → attention → layers → output distribution.”
  - Nano Banana variant: “Minimal pipeline diagram with 5 labeled boxes and arrows; enterprise styling.”
  - Label: flowchart
  - Placement: Slide 1 or 4
- **Table graphic:** Missing vs conflicting context diagnosis
  - Prompt: “A clean 2-column table titled ‘Diagnosing failures’: Missing context vs Conflicting context; include symptoms and fixes.”
  - Nano Banana variant: “Create a minimal table infographic with two columns: Missing vs Conflicting; add icons (question mark vs warning).”
  - Label: infographic
  - Placement: Slide 6

### 6) Safety & risk callouts
- **Relevant risks:** Overconfidence; treating model as source of truth; context poisoning via irrelevant/untrusted text.
- **Mitigations to mention:** Curate context; isolate untrusted input; demand assumptions; verify with tests/reviews.
- **Critical safety concepts:** Sets up “untrusted content isolation” for injection defenses.

