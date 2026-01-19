
# Lecture Series Syllabus —  Episodes (Enterprise AI SDLC)

Design intent:
- Each episode is around **23 minutes** so it fits calendar blocks and stays “watchable”
- Episodes align to the 10-week program but can also stand alone as a library
- Each episode ends with a concrete “do this next” action

## Episode map (24 episodes)

### Week 1 — Foundations of enterprise-safe AI SDLC
1. **The enterprise AI SDLC loop (plan → diff → review → ship)**  
   Output: personal workflow checklist + baseline measurement plan  
2. **Prompt hygiene + output contracts (make AI deterministic)**  
   Output: prompt-pattern entry (template filled)  
3. **Permissions, data classes, and redaction rules (don’t get fired)**  
   Output: redaction checklist + “allowed vs disallowed” examples  

### Week 2 — Planning mode and task decomposition
4. **Plan mode deep dive: from vague ticket to atomic tasks**  
   Output: task list + acceptance criteria  
5. **Diff-first development: how to review AI changes safely**  
   Output: review checklist + “stop conditions”  
6. **PR narration: what changed / why / risk / how tested**  
   Output: PR narration template filled for a sample change  

### Week 3 — Testing acceleration (without shipping garbage)
7. **Test strategy: where to spend test effort (unit vs integration)**  
   Output: test plan for a module  
8. **AI-generated unit tests: edge cases + brittleness management**  
   Output: 10 test cases + rationale  
9. **Coverage as a lever: baseline, target, and “coverage delta report”**  
   Output: coverage delta report template filled  

### Week 4 — Docs and architecture extraction
10. **Docs-from-code: architecture README that engineers will read**  
    Output: architecture README skeleton  
11. **ADRs: capturing decisions and trade-offs quickly**  
    Output: ADR v1  
12. **Diagramming basics: C4-style diagrams without perfectionism**  
    Output: diagram outline + labels (no fancy tooling required)  

### Week 5 — Production codebase analysis and risk
13. **Codebase mapping: dependencies, boundaries, "blast radius"**
    Output: dependency map notes + boundary list  
14. **Risk-ranked backlog: picking “safe PR” candidates**  
    Output: ranked backlog (top 10)  
15. **Large codebase navigation techniques using AI**  
    Output: “codebase questions” prompt library entry  

### Week 6 — Safe PR strategy (scaffolding-first)
16. **Scaffolding-only PRs: improving safety without changing logic**  
    Output: safe PR plan + rollout steps  
17. **Refactoring with AI: sequencing changes to reduce risk**  
    Output: refactor proposal with PR slices  
18. **Operational readiness: runbooks, logging standards, error taxonomies**  
    Output: runbook checklist  

### Week 7 — CI/CD and quality gates
19. **Quality gates that don’t break teams: lint/test/coverage thresholds**  
    Output: gate configuration plan  
20. **Pipeline hygiene: PR checks, failure triage, and developer UX**  
    Output: “how to fix failures” guide  
21. **Release notes + change tracking: automated narration**  
    Output: release note template + generation prompt  

### Week 8 — Observability patterns that matter
22. **Structured logging + correlation IDs (the minimum viable observability)**  
    Output: log field schema + correlation strategy  
23. **Tracing and metrics (when to use what)**  
    Output: instrumentation plan for endpoints  

### Week 9 — Security, MCP/tooling, prompt injection
24. **Tool calling/MCP concepts + prompt injection defenses**  
    Output: prompt-injection threat checklist + mitigations  

## How to deliver the lecture series
- For live cohorts: assign 2–3 episodes/week (total ~1 hour) and then run the lab.
- For asynchronous: publish 1 episode per day (Mon–Thu) and run lab blocks on Tue/Thu.

## Notes on “MCP/tool calling”
This syllabus treats “MCP/tool calling” conceptually (permissions, tool surfaces, injection risk).  
If the client environment doesn’t allow tool calling, the same safety rules apply to any “agent CLI” or plugin-based execution.
