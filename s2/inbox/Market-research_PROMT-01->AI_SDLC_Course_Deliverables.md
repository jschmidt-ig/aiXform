# AI SDLC Course Productization Deliverables

## Executive Summary

- Corporate AI training pricing varies widely: self‑paced subscriptions cost **$200–$600 per user/year**【782676473835191†L173-L179】【736099771441487†L340-L391】, cohort‑based programs cost **$2k–$7k per seat**【110760513825565†L104-L127】【464633521006769†L33-L44】, and bespoke packages can reach **$12k–$250k**【59280895032307†L173-L242】.
- Instructor involvement is the biggest cost driver; short workshops (1–2 days) cost **$500–$1.5k**【383516932941829†L585-L675】【110760513825565†L19-L70】, while high‑touch multi‑week bootcamps command **$5k+**.
- Successful training products use tiered structures: basic self‑paced, hybrid community/office hours, and premium coaching with capstones【565410578974657†L86-L90】.
- Gross margin targets of **50–70 %** are recommended for scalable services【479414317311090†L94-L110】.
- Tier names should be professional or role‑based (e.g., Foundation, Practitioner, Architect) rather than martial‑arts colors【674820522831237†L74-L80】.
- KPIs should track cycle time, deployment frequency, PR frequency, escaped defects, documentation completeness, test coverage, adoption and developer satisfaction【452914221545876†L552-L669】【533174244837830†L90-L104】.
- Security constraints require off‑network sandboxes and approved models only; tool approvals may delay initial weeks.
- Brownfield support is critical; start with safe greenfield examples while waiting for tool access.
- Team packs and enterprise bundles encourage broader adoption and provide predictable revenue; gating advanced tiers ensures readiness.
- Recording the consulting engagement and capturing code samples will create reusable assets for the product.

## Market Map (Comparables)

| Company                      | Offer type                | Delivery model            | Pricing signals                                                                                      | Tiering patterns           | Notes                      |
| ---------------------------- | ------------------------- | ------------------------- | ---------------------------------------------------------------------------------------------------- | -------------------------- | -------------------------- |
| Coursera for Business        | Online courses            | Self‑paced + labs         | $399/user/year【782676473835191†L173-L179】                                                            | Per‑seat; enterprise quote | Well adopted; assessments. |
| DataCamp Teams               | AI skills platform        | Self‑paced                | $14/user/month【283839364772207†L622-L672】                                                            | Team vs enterprise         | Hands‑on coding.           |
| Pluralsight AI+Data          | Tech e‑learning           | Self‑paced + labs         | $399/user/year【736099771441487†L340-L391】                                                            | Content breadth tiers      | Labs & analytics.          |
| O’Reilly Learning            | Books/courses/live events | Self‑paced & live         | $399/user/year【385482733753882†L169-L172】                                                            | Team/enterprise            | Books & videos.            |
| Udemy Business               | Mass‑market e‑learning    | Self‑paced                | $30/user/month【431645990909511†L215-L219】                                                            | Team vs enterprise         | Large library.             |
| Udacity Teams                | Nano‑degrees              | Self‑paced + mentors      | $2,390–4,788/user/year【448964155751978†L567-L571】                                                    | Individual vs team vs pro  | Premium mentoring.         |
| Codecademy Teams             | Coding practice           | Self‑paced exercises      | $25/seat/month【347070739455114†L64-L69】                                                              | Discounts for size         | Limited AI content.        |
| FourthBrain                  | LLM workshops             | Instructor‑led            | $500 per person; $2,000 for 3‑wk program【110760513825565†L19-L70】【110760513825565†L104-L127】         | Per‑workshop vs team       | High touch.                |
| Improving.com                | Corporate workshops       | Private or per‑student    | $495–$3,500【593427725835286†L63-L74】【593427725835286†L159-L190】                                      | Duration‑based             | Certifications.            |
| NVIDIA DLI                   | AI & GenAI courses        | Self‑paced + workshops    | $30–$90 (3–8 hr); $500 (8 hr); $5,500 (40+ hr)【383516932941829†L585-L675】【383516932941829†L660-L740】 | Duration & format tiers    | Labs & varied curriculum.  |
| MentorCruise                 | Mentoring sessions        | Live coaching             | $149 per session【57960484681941†L134-L146】                                                           | Pay‑per‑session            | Flexible but costly.       |
| Azure AI Boot Camp           | Boot camp                 | Instructor‑led            | $2,695 for 3 days【282452085100280†L103-L129】                                                         | Single tier                | Azure-focused.             |
| Workforce Institute Bootcamp | 14‑wk bootcamp            | Instructor‑led + projects | $7,000【464633521006769†L33-L44】                                                                      | Single tier                | Comprehensive training.    |
|                              |                           |                           |                                                                                                      |                            |                            |
|                              |                           |                           |                                                                                                      |                            |                            |

## Pricing Benchmarks

- **Self‑paced subscription:** $200–$600 per seat/year【782676473835191†L173-L179】【736099771441487†L340-L391】.
- **Team plans:** $14–$30 per seat/month (~$168–$360/year)【283839364772207†L622-L672】【431645990909511†L215-L219】.
- **Short workshops (1–2 days):** $500–$1.5k per person【383516932941829†L585-L675】.
- **Cohort programs (3–14 weeks):** $2k–$7k per seat【110760513825565†L104-L127】【464633521006769†L33-L44】.
- **Enterprise/executive packages:** $12k–$250k; executive seats can cost $15k–$50k【59280895032307†L173-L242】【59280895032307†L251-L337】.
- Cost drivers: instructor time, program length, certification, and customization.

## Packaging Patterns

- **Basic/self‑paced**: materials, labs, quizzes; high margin; entry level.
- **Hybrid/community**: adds forums, Q&A sessions, group office hours; mid‑price.
- **Premium/coaching**: personalized coaching, project feedback, capstone; limited seats; high price【565410578974657†L86-L90】.
- **Gating**: advanced tiers require completion of earlier ones; cohort sizes shrink as tier increases.
- **Bundles**: combine seats from multiple tiers to offer enterprise discounts.

## Naming Patterns

- Professional: Foundation, Practitioner, Specialist, Professional, Expert, Mastery, Executive, Accelerator.
- Technical: Explorer, Builder, Innovator, Architect, Engineer, Operator, Strategist.
- Playful: Trailblazer, Pioneer, Visionary, Catalyst, Quantum, Nova, Vanguard.
- Avoid generic belt colors; choose role‑oriented or aspirational names【674820522831237†L74-L80】【674820522831237†L139-L143】.

## KPI Menu (Controllable vs Lagging)

- **Cycle time** (controllable): commit → deploy【452914221545876†L552-L669】.
- **Lead time for changes** (controllable) & **Deployment frequency** (lagging)【452914221545876†L552-L669】.
- **PR frequency** (controllable)【751564058249147†L50-L80】.
- **Escaped defects** (lagging)【658254506190630†L54-L83】.
- **Change failure rate** & **MTTR** (lagging)【452914221545876†L552-L669】.
- **Test coverage** (controllable) & **Documentation completeness** (controllable).
- **Developer satisfaction/NPS** (lagging)【533174244837830†L90-L104】.
- **Adoption metrics** (controllable) & **Collaboration metrics** (lagging)【533174244837830†L134-L190】.

## Recommendations

1. **Three‑tier model**: Foundations (self‑paced), Professional (hybrid), Enterprise Accelerator (deep coaching).  Offer team packs; price per participant: $300–$500; $2k–$3k; $8k–$15k (or $30k–$50k per team).
2. **Gross margin targets**: 50–70 %【479414317311090†L94-L110】; minimise instructor hours per seat via asynchronous content and group coaching.
3. **Names**: Use professional or role‑oriented names (Foundation, Innovator, Architect); avoid belt colours.
4. **Team bundles & flexible durations**: Provide 10‑week standard cohort, optional 6‑week bootcamp, 14‑week extended program; combine seats across tiers in bundles.
5. **Metrics dashboards**: Track cycle time, throughput, quality, documentation, adoption and satisfaction; provide baseline/mid/end course reports.
6. **Content capture pipeline**: Record demos and Q&A; collect code samples; convert to reusable assets; tag by module.
7. **Scaling plan**: After MVP, build a six‑month v2 with additional languages (Java, .NET), cross‑cloud examples (Azure, AWS), and role‑specific tracks (SWE vs infra).

## Risk Register & Mitigations

| Risk | Mitigation |
| --- | --- |
| **Security & data** | Use isolated sandboxes; keep code on client servers; approved models only; prompt review. |
| **Tool access delays** | Start with offline modules; provide containerised environment; coordinate early with IT. |
| **Low adoption** | Shorter lessons, milestones, gamification; manager nudges; dashboards. |
| **Executive buy‑in** | ROI models and early wins; involve leaders in kick‑off. |
| **Delivery capacity** | Limit cohort sizes; maintain coach ratios; schedule carefully. |
| **Environment complexity** | Use templates; pre‑course code analysis; buffer time. |
| **IP concerns** | SOW clauses for anonymising and reusing materials; client approvals. |

## Draft SOW Addendum Outline

1. **Scope & tiers**: Define purchased tier(s); list deliverables (content access, sandbox, office hours, coaching, capstone).
2. **Inclusions**: Participant access, labs, weekly materials, assessments, metrics dashboards, executive briefings; content capture rights.
3. **Exclusions**: No on‑site work; no client network modifications; no unapproved tool integration; no bespoke code beyond labs.
4. **Client responsibilities**: Provide repo access or anonymised samples; ensure participant time allocation; secure model approvals; attend briefings; support security reviews.
5. **Assumptions/dependencies**: Tool approvals within two weeks; baseline skills; timeline may adjust due to security reviews; IP can be anonymised.
6. **Success criteria**: Improved cycle time, throughput, test coverage, documentation; adoption rates; satisfaction scores; capstone completion; final report.

