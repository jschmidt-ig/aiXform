# Team AI Playbook

**Team:** [Team Name]
**Date:** [Date]
**Version:** [1.0]

---

## Purpose

This playbook documents how our team uses AI-assisted development tools. It captures our agreed practices, rules, and workflows to ensure consistent, safe, and effective use of AI in our development process.

> **Note:** This is a living document. Update it as we learn and our practices evolve.

---

## 1. Our AI Tools

### Approved Tools
List the AI tools approved for use by your team:

| Tool | Use Case | Access Level |
|------|----------|--------------|
| [e.g., Claude Code CLI] | [e.g., Code generation, refactoring] | [e.g., All team members] |
| | | |
| | | |

### Not Approved / Restricted
Tools or uses that are NOT approved:

| Tool/Use | Reason |
|----------|--------|
| [e.g., Free-tier public APIs] | [e.g., Data leaves our environment] |
| | |

---

## 2. When to Use AI

### Good Use Cases
AI assistance works well for our team when:

- [ ] [e.g., Writing boilerplate code]
- [ ] [e.g., Generating unit tests for existing code]
- [ ] [e.g., Refactoring well-understood code]
- [ ] [e.g., Writing documentation]
- [ ] [e.g., Exploring unfamiliar APIs/libraries]
- [ ] [Add your own...]

### When NOT to Use AI (or Use with Extra Caution)
Be careful or avoid AI for:

- [ ] [e.g., Security-critical code without thorough review]
- [ ] [e.g., Code involving sensitive data handling]
- [ ] [e.g., Architectural decisions without team discussion]
- [ ] [e.g., Areas where we lack expertise to review output]
- [ ] [Add your own...]

### Decision Guide
```
Before using AI, ask:
1. Do I understand this domain well enough to review the output?
2. Is the data I'm providing safe to include?
3. Would a mistake here be caught before production?
4. Am I using AI to learn, or to skip learning?
```

---

## 3. Data & Security Rules

### What CAN go into AI prompts
- [ ] Public documentation and APIs
- [ ] Open-source code references
- [ ] Sanitized/redacted code snippets
- [ ] Generic error messages
- [ ] [Add your own...]

### What CANNOT go into AI prompts
- [ ] Customer data (PII, PHI, etc.)
- [ ] Credentials, API keys, secrets
- [ ] Internal security configurations
- [ ] Proprietary business logic (if restricted)
- [ ] [Add your own based on your organization's policy...]

### Redaction Practices
Before including code in prompts:
1. [e.g., Replace real customer IDs with placeholders]
2. [e.g., Remove connection strings and credentials]
3. [e.g., Generalize business-specific terminology if needed]

---

## 4. Code Review Practices

### AI-Generated Code Review Checklist
When reviewing PRs that include AI-generated code:

- [ ] **Correctness:** Does it actually do what was intended?
- [ ] **Edge cases:** Are edge cases handled appropriately?
- [ ] **Security:** Any security concerns (injection, auth, etc.)?
- [ ] **Tests:** Are there adequate tests? Do they test the right things?
- [ ] **Readability:** Is the code understandable to the team?
- [ ] **Maintainability:** Will we be able to maintain this?
- [ ] **Fits our patterns:** Does it follow our existing conventions?

### PR Narration Standard
PRs with significant AI assistance should include:

```markdown
## What
[What changed]

## Why
[Why this change was needed]

## AI Assistance
[How AI was used - e.g., "Generated initial test suite, then manually refined"]

## Risk
[What could go wrong, how it was mitigated]

## Testing
[How it was tested]
```

### Review Rigor by Risk Level

| Risk Level | Examples | Review Requirement |
|------------|----------|-------------------|
| Low | Docs, comments, simple tests | Standard review |
| Medium | Business logic, refactoring | Careful review + manual testing |
| High | Auth, payments, data handling | Senior review + thorough testing |

---

## 5. Quality Gates

### Before Merging AI-Assisted Code

- [ ] Code compiles and passes linting
- [ ] All existing tests pass
- [ ] New tests added for new functionality
- [ ] PR narration complete (including AI disclosure)
- [ ] At least one human reviewer approved
- [ ] [Add your own gates...]

### Automated Checks
Our CI/CD pipeline enforces:
- [e.g., Unit test pass rate]
- [e.g., Code coverage threshold]
- [e.g., Static analysis / linting]
- [Add your own...]

---

## 6. Team Workflows

### Workflow 1: [e.g., Test Generation]
**When:** [e.g., Adding tests to existing code]
**Process:**
1. [Step 1]
2. [Step 2]
3. [Step 3]

### Workflow 2: [e.g., Code Refactoring]
**When:** [e.g., Cleaning up legacy code]
**Process:**
1. [Step 1]
2. [Step 2]
3. [Step 3]

### Workflow 3: [e.g., Documentation]
**When:** [e.g., Documenting a service or API]
**Process:**
1. [Step 1]
2. [Step 2]
3. [Step 3]

---

## 7. Learning & Improvement

### How We Learn
- [e.g., Share interesting AI interactions in team channel]
- [e.g., Monthly retrospective on AI practices]
- [e.g., Maintain a "tips and tricks" doc]

### What We Track
- [e.g., Time saved on specific tasks]
- [e.g., Quality of AI-generated code]
- [e.g., Cases where AI output was wrong/misleading]

### Playbook Updates
This playbook is updated:
- [e.g., After each sprint retrospective]
- [e.g., When we discover new best practices]
- [e.g., When organizational policy changes]

**Owner:** [Name/Role responsible for maintaining this doc]

---

## 8. Escalation & Questions

### When to Escalate
Escalate to [person/role] when:
- Uncertain about data classification
- AI suggests something that seems risky
- Need approval for new tools or uses
- Compliance or legal questions arise

### Resources
- Organization AI Policy: [link]
- Security team contact: [contact]
- AI tools support: [contact]

---

## 9. Team Agreement

We, the [Team Name] team, agree to follow the practices in this playbook.

| Name | Role | Date |
|------|------|------|
| | | |
| | | |
| | | |

---

## Changelog

| Version | Date | Changes | Author |
|---------|------|---------|--------|
| 1.0 | [Date] | Initial version | [Name] |
| | | | |
