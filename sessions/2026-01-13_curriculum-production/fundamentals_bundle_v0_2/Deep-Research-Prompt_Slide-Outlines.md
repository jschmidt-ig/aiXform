ChatGPT Folder > s6 - Course Syllabus Blocking > Deep-Research-Prompt_Slide-Outlines.md

# Deep Research Prompt Template — Slide Outlines + Demos (for each Fundamentals session)

Use this prompt with:
- **Gemini Deep Research** (research agent)
- **ChatGPT Deep Research** (research agent)

## How to use (recommended workflow)
1) **Start small:** Run this prompt for **Sessions 1–2 only** (or 1–3).  
2) Review output for: slide count, depth, demo feasibility, and enterprise-safety framing.  
3) Adjust the prompt variables (below) and rerun for **Sessions 3–5**.  
4) Once the style is correct, run it for the remaining sessions in batches (e.g., 4 sessions per run).  
5) Keep a “Slide Standard” doc: what you liked from outputs; paste it into the prompt as an additional constraint in later runs.

## Variables you should set before each run
- **SESSIONS_TO_GENERATE:** e.g., `1–2` or `3–5`
- **AUDIENCE_LEVEL:** e.g., `mid/senior software engineers (enterprise)`  
- **TOOLING_CONTEXT:** e.g., `CLI-first later (Claude Code CLI), but Fundamentals is lecture-only`  
- **STYLE:** e.g., `practical, minimal fluff, diagrams where helpful`  
- **SLIDE_DENSITY:** e.g., `8–12 slides per 20–30 min session`  
- **DEMO_MODE:** `lecture-only demos (show commands/snippets on slides; no execution required)`

---

## Prompt (copy/paste)

You are a curriculum designer and technical instructor for an enterprise AI SDLC course.

GOAL
Create a slide-outline package for the following course sessions so I can build a full lecture deck. The output must be detailed enough to fill 20–30 minutes per session and must include concrete examples, code snippets/commands for on-slide demos, and suggested diagrams/graphics.

CONTEXT
- The course is **AI SDLC Fundamentals (2 weeks)**. These sessions are **LECTURE-ONLY**. Learners will not run tools during Fundamentals.
- Later phases will use CLI harnesses (e.g., Claude Code CLI), API calls (e.g., cURL), and tool calling. But here: show commands/snippets as examples; do not require execution.
- Enterprise constraints are real: no external SaaS, no code upload, approved models only, PHI/PII sensitivity, security reviews.

SESSIONS TO GENERATE
{SESSIONS_TO_GENERATE}

AUDIENCE
{AUDIENCE_LEVEL}

STYLE
- Tone: clear, direct, practical.
- Prefer diagrams and tables over long text.
- Include 1–2 “common misconceptions” callouts per session.
- Include security framing where relevant.
- Assume 20–30 minutes and target {SLIDE_DENSITY} slides per session.

INPUT SYLLABUS (authoritative)
Use the session titles and intent from this syllabus excerpt:

(Include the session list you’re generating here, copied from my syllabus)
- Session X — Title: ...
- Session Y — Title: ...
(etc.)

DELIVERABLES (for EACH session, in this exact structure)

1) Session summary
- Title
- One-sentence purpose
- 3 learning objectives
- “If learners only remember 1 thing” line

2) Slide-by-slide outline
For each slide:
- Slide title
- Key bullets (max 5)
- Speaker notes (what I should say; concise)
- Visual/diagram suggestion (if any)
- Time estimate (minutes)

3) Demo-in-lecture plan (no execution required)
- 1–2 demo moments that fit on slides
- Provide:
  - Command snippets (e.g., cURL examples) OR
  - CLI transcript snippets (e.g., Claude Code CLI hypothetical output) OR
  - Pseudocode for tool-calling JSON
- Include “what to point out” talking notes and “what could go wrong” talking notes

4) Examples bank
- 2–3 worked examples per session:
  - one “good” example
  - one “bad” example and why it fails
  - one “enterprise-safe” example with redaction/constraints

5) Graphics pack (image/diagram prompts)
Provide prompts for generating visuals for the deck:
- 2–4 diagram ideas per session (e.g., transformer overview, agentic loop, context assembly)
- For each, give:
  - A plain-English image prompt (for any image generator)
  - A “Nano Banana” prompt variant (keep it generic: JSON optional; include a text-only version too)
  - Label: (diagram / infographic / icon / flowchart)
  - Suggested slide placement

6) Safety & risk callouts
- Relevant risks (prompt injection, tool permissioning, data exposure) for this session
- Mitigations to mention (lecture-only)
- Identify which points should be treated as “critical safety” concepts

7) References (optional)
- If you cite any external claims, include a short reference list with titles only (no URLs needed).

QUALITY BAR
- This must be teachable and flow as a lecture.
- Avoid generic filler; every slide should earn its place.
- Do not assume the learner can run any tools during Fundamentals.
- Avoid recommending unsafe practices (e.g., copying sensitive code into prompts).
- Prefer examples that match enterprise reality (policies, approvals, auditability, least privilege).

OUTPUT FORMAT
- Use clear headings.
- Use numbered lists where appropriate.
- Do not include long essays; provide slide-ready structure.

---

## Notes for Gemini vs ChatGPT runs
- If the tool supports it, attach or paste the syllabus section for the sessions you’re generating.
- If output is too verbose: reduce slide count and force “max 5 bullets per slide.”
- If output is too shallow: increase slide density to 10–14 and ask for 2 demos per session.
