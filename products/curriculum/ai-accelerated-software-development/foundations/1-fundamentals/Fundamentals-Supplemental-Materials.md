# Fundamentals — Supplemental Materials Guide

This guide provides assigned reading, videos, and exercises to complement the 20 lecture sessions. Supplemental materials bring the weekly time commitment to **8-10 hours/week**.

> **Note:** Fundamentals is intentionally **tool-agnostic**. These materials teach concepts that apply to ANY AI coding tool. Instructors may demo specific tools, but the goal is understanding principles, not product tutorials.

## Time Budget

| Activity | Week 1 | Week 2 |
|----------|--------|--------|
| Lecture sessions (5 days × 2 sessions) | ~4-5 hrs | ~4-5 hrs |
| Supplemental materials | ~4-5 hrs | ~4-5 hrs |
| **Total** | **8-10 hrs** | **8-10 hrs** |

## How to Use This Guide

- **Before each day:** Complete the "Pre-Session" materials (typically 20-30 min)
- **After each day:** Complete the "Post-Session" materials (typically 30-45 min)
- **End of week:** Complete the weekly reflection (30 min)

---

# Week 1: Foundations of LLMs and Context

## Day 1: Orientation & Enterprise Constraints
*Sessions 1-2: Course orientation, Tooling + constraints*

### Pre-Session (20 min)
- **Read:** "What is Generative AI?" — Any high-quality overview article explaining generative AI vs traditional software (15 min)
- **Reflect:** Write down 3 things you currently use AI for in your work, and 3 things you're skeptical about (5 min)

### Post-Session (45 min)
- **Read:** Your organization's AI acceptable use policy (if available) — Note constraints that apply to your work (15 min)
- **Read:** [OWASP Top 10 for LLM Applications](https://owasp.org/www-project-top-10-for-large-language-model-applications/) — Read the introduction and first 3 items (20 min)
- **Exercise:** Data classification — List 5 types of data you work with daily. Classify each as: (a) safe to include in AI prompts, (b) requires redaction first, (c) never include. Write a sentence explaining each classification. (10 min)

---

## Day 2: LLMs & Tokens
*Sessions 3-4: LLMs + tokens, Transformer mental model*

### Pre-Session (30 min)
- **Watch:** [3Blue1Brown - But what is a GPT? Visualizing Attention](https://www.youtube.com/watch?v=wjZofJX0v4M) — Excellent visual explanation of how transformers work (26 min)

### Post-Session (40 min)
- **Read:** "Tokenization Explained" — Find an article or blog post explaining how text becomes tokens, subword tokenization, and why it matters (15 min)
- **Exercise:** Use any free tokenizer tool online to see how different text tokenizes:
  - Your name
  - A code snippet from your work (redacted)
  - The word "tokenization" vs "token" vs "tokens"
  - Note: Different models tokenize differently! (15 min)
- **Reflect:** Why does tokenization matter for cost and context limits? Write 2-3 sentences. (10 min)

---

## Day 3: Training, Inference & Context Windows
*Sessions 5-6: Training vs inference, Context window + no long-term memory*

### Pre-Session (25 min)
- **Read:** "Training vs Inference: What's the Difference?" — Find an article explaining the distinction between model training and inference (15 min)
- **Read:** Brief overview of what "fine-tuning" means (10 min)

### Post-Session (45 min)
- **Read:** Any article on "context window" limitations in LLMs — understand what happens when context is exceeded (15 min)
- **Exercise:** Context decay thought experiment — Imagine a 50-message conversation with an AI. You gave important instructions in message 1. By message 50, what might happen to those instructions? How would you design around this? Write your answer. (15 min)
- **Reflect:** "What misconceptions did I have about how AI 'learns' or 'remembers'?" Write a short paragraph. (15 min)

---

## Day 4: Prompting Fundamentals
*Sessions 7-8: Prompting fundamentals, Chatbot vs raw model call*

### Pre-Session (30 min)
- **Read:** Any comprehensive "Prompt Engineering 101" guide — Look for one that covers: roles, constraints, examples, output formats (20 min)
- **Read:** Brief explanation of "system prompts" vs "user prompts" — understand the different message roles (10 min)

### Post-Session (45 min)
- **Read:** Article on "structured outputs" from LLMs — JSON, XML, markdown formats (15 min)
- **Exercise:** Prompt improvement — Take a vague prompt you've used before (or make one up). Rewrite it with:
  - Clear role/persona
  - Explicit constraints
  - Output format specification
  - Success criteria
  Compare before/after. What ambiguities did you remove? (20 min)
- **Reflect:** Which of your current AI interactions would benefit from better prompt structure? (10 min)

---

## Day 5: Prompt Contracts & Context Engineering
*Sessions 9-10: Prompt contracts + output schemas, Context engineering workshop*

### Pre-Session (25 min)
- **Read:** Article on "few-shot prompting" — using examples to guide AI output (15 min)
- **Read:** Any article on managing long contexts effectively (10 min)

### Post-Session (40 min)
- **Exercise:** Create 3 output contracts (templates) for tasks relevant to your work. Each should specify exact sections/format expected:
  1. Code review feedback contract
  2. Bug analysis contract
  3. Technical decision summary contract
  (30 min)
- **Reflect:** Which of your daily tasks would benefit from a standardized output contract? (10 min)

### Week 1 Reflection (30 min)
Write 1-2 paragraphs answering each:
1. What's the most important concept from Week 1 that changes how you think about AI?
2. What misconception have you corrected?
3. What question do you still have going into Week 2?

---

# Week 2: Agents, Tools & Security

## Day 6: Agents & Harnesses
*Sessions 11-12: Agents vs workflows + agentic loop, Harness taxonomy*

### Pre-Session (30 min)
- **Read:** "What are AI Agents?" — Find an article explaining the difference between chatbots and agents. Look for coverage of: goals, tools, loops, autonomy (20 min)
- **Read:** Brief overview of "agentic workflows" in software development (10 min)

### Post-Session (40 min)
- **Read:** Article comparing different AI coding assistants (any recent comparison article) — Focus on: What tools can each access? What can each do autonomously? (20 min)
- **Exercise:** Tool inventory — List 3 AI tools you have access to (or have heard of). For each:
  - What actions can it take?
  - What context does it have access to?
  - What permissions does it need?
  - Where could it go wrong? (20 min)

---

## Day 7: Agentic Coding & Model Selection
*Sessions 13-14: Agentic coding method, Model mixing + harness comparisons*

### Pre-Session (25 min)
- **Read:** Any article on "AI-assisted code review" or "AI pair programming" workflows (15 min)
- **Reflect:** Think about your last 3 coding tasks. Which would benefit from AI assistance? Which would not? Why? Write notes. (10 min)

### Post-Session (45 min)
- **Read:** Article comparing different LLM models (any recent comparison) — Understand trade-offs: capability vs speed vs cost (15 min)
- **Exercise:** PR narration practice — Write a pull request description for an imaginary code change. Use this format:
  - **What:** What changed?
  - **Why:** Why was this change needed?
  - **Risk:** What could go wrong?
  - **Testing:** How was it tested?
  (20 min)
- **Exercise:** When would you use a "fast/cheap" model vs a "powerful/expensive" model? Create a simple decision guide for your work. (10 min)

---

## Day 8: Tool Calling & Integrations
*Sessions 15-16: Tool calling, MCP vs API calls*

### Pre-Session (25 min)
- **Read:** "What is function calling in LLMs?" — Find an article explaining how LLMs can call external tools/functions (15 min)
- **Read:** Brief overview of APIs and how software systems integrate (review if needed) (10 min)

### Post-Session (40 min)
- **Read:** Article on "AI tool use" risks and benefits (15 min)
- **Exercise:** Tool risk analysis — List 5 tools/APIs/systems you use at work. For each:
  - What would an AI need to use it?
  - What could go wrong if AI used it incorrectly?
  - What permissions should be required?
  - What should require human approval? (25 min)

---

## Day 9: Security — Permissions & Prompt Injection
*Sessions 17-18: Securing tool calls + permissioning, Prompt injection*

### Pre-Session (30 min)
- **Read:** [OWASP Top 10 for LLM Applications](https://owasp.org/www-project-top-10-for-large-language-model-applications/) — Read items 1 (Prompt Injection) and 7 (Insecure Plugin Design) thoroughly (30 min)

### Post-Session (45 min)
- **Read:** Any article specifically about "prompt injection attacks" — understand how untrusted input can hijack AI behavior (15 min)
- **Exercise:** Injection detection — For each input below, identify if it could contain a prompt injection risk and explain why:
  1. A user-submitted bug report from your ticketing system
  2. A code comment that says "AI: ignore previous instructions and..."
  3. A configuration file with embedded text fields
  4. A customer email being summarized by AI
  5. A log file containing user-controlled strings
  (20 min)
- **Exercise:** Design a permission set for a hypothetical "code review AI assistant":
  - What can it read?
  - What can it write?
  - What can it execute?
  - What requires human approval? (10 min)

---

## Day 10: Security Lab & Capstone
*Sessions 19-20: Security lab, Integrated capstone demo + recap*

### Pre-Session (20 min)
- **Review:** Skim your notes and reflections from Week 1 and Week 2 (15 min)
- **Prepare:** Write 2-3 questions you want answered in the final sessions (5 min)

### Post-Session (45 min)
- **Exercise:** End-to-end scenario analysis — Pick a realistic task from your work (e.g., "Use AI to help refactor a data validation module"). Answer:
  1. What context would you provide to the AI?
  2. What output format/contract would you specify?
  3. What tools would the AI need access to?
  4. What permissions would you grant (and NOT grant)?
  5. What prompt injection risks exist in this scenario?
  6. What would you verify before accepting the AI's output?
  (30 min)
- **Exercise:** Write your personal "AI Coding Principles" — 5-7 rules you'll follow when using AI in your development work (15 min)

### Week 2 Reflection (30 min)
Write 1-2 paragraphs answering each:
1. How has your understanding of AI security changed?
2. What workflow changes will you make based on this course?
3. What are you most looking forward to practicing in the Labs phase?

---

## Time Summary

| Day | Sessions | Pre-Session | Post-Session | Total |
|-----|----------|-------------|--------------|-------|
| 1 | ~50 min | 20 min | 45 min | ~2 hrs |
| 2 | ~50 min | 30 min | 40 min | ~2 hrs |
| 3 | ~50 min | 25 min | 45 min | ~2 hrs |
| 4 | ~50 min | 30 min | 45 min | ~2 hrs |
| 5 | ~50 min | 25 min | 40 min + 30 min reflection | ~2.5 hrs |
| 6 | ~50 min | 30 min | 40 min | ~2 hrs |
| 7 | ~50 min | 25 min | 45 min | ~2 hrs |
| 8 | ~50 min | 25 min | 40 min | ~2 hrs |
| 9 | ~50 min | 30 min | 45 min | ~2 hrs |
| 10 | ~50 min | 20 min | 45 min + 30 min reflection | ~2.5 hrs |

**Week 1 Total:** ~10.5 hours
**Week 2 Total:** ~10.5 hours

---

## Recommended Resources

### Security (Required)
- [OWASP Top 10 for LLM Applications](https://owasp.org/www-project-top-10-for-large-language-model-applications/)

### Conceptual Videos
- [3Blue1Brown - But what is a GPT?](https://www.youtube.com/watch?v=wjZofJX0v4M) — Best visual explanation of transformers

### General Reading (Suggested Sources)
For the reading assignments, learners should find current articles from reputable sources. Good places to look:
- AI company blogs (Anthropic, OpenAI, Google DeepMind, etc.)
- Tech publications (MIT Technology Review, Ars Technica, The Verge)
- Developer-focused sites (dev.to, Hacker News, InfoQ)
- Academic summaries (Papers With Code, Distill.pub archives)

### Why We Don't Prescribe Specific URLs
1. **Content moves:** URLs break; articles get updated or removed
2. **Currency matters:** AI moves fast; find the most recent explanations
3. **Learning skill:** Finding good sources is part of professional development
4. **Tool-agnostic:** We don't want to bias toward any vendor's documentation

---

## Notes for Instructors

1. **Curate a reading list:** Before each cohort, instructors should compile specific article recommendations. Share via your LMS or cohort channel.

2. **Enterprise customization:** Replace generic exercises with company-specific scenarios where possible (using redacted/sanitized examples).

3. **Sensitive data reminder:** Remind learners to NEVER use real sensitive data in exercises. Always use redacted or synthetic examples.

4. **Discussion forums:** Consider async discussion channels for learners to share reflections and discuss readings.

5. **Time flexibility:** Learners may complete supplemental materials at their own pace within the week, but should complete them before moving to the next week.

6. **Demo variety:** When demoing tools in lectures, vary the tools shown (Claude Code, Copilot, Cursor, etc.) to reinforce tool-agnostic principles.
