# Business Analyst Challenge – Chemical Injection Equipment Management System (CIEMS)

Specification of a web system to register chemical tanks, wells and pumps, associate tanks to wells, and monitor injection rate, estimated chemical consumption per well and tank autonomy (days until 20% of capacity) for oil production sites.

**Author:** Amanda Evangelista Lima · amandaelima1@gmail.com · [https://www.linkedin.com/in/amanda-evangelista-lima-3056b11aa/?isSelfProfile=true]
**Version:** 1.0 · **Language of the documentation:** English

---

## 1. Files in this repository

Each artifact requested in the challenge is delivered in its own file.

| # | File | Challenge artifact |
|---|------|--------------------|
| 1 | `01_Project_Deliverables.docx` | List of project deliverables |
| 2 | `02_Project_Activities_by_Phase.docx` | List of activities organized by phase (3 phases) |
| 3 | `03_Requirements_and_Business_Rules.docx` | Requirements and business rules (also includes user stories, use cases, data model, open questions and traceability matrix) |
| 4 | `04_LoFi_Prototype.pdf` | Lo-Fi prototype (7 screens + navigation flow) |
| 5 | `05_Methodology_Prioritization_and_KPIs.docx` | Suggested features, KPIs, development methodology and prioritization simulation |
| 6 | `README.md` | This file |

Suggested reading order: 03 → 04 → 05, using 01 and 02 as project context.

---

## 2. General comments on my choices

**Interpreting the brief.** The brief is short on purpose, so I made my interpretations explicit instead of hiding them. Every assumption is recorded in the *Assumptions and Open Questions* table (document 03, section 3) with the working decision I took and the impact, so they can be validated with the client.

**Traceability first.** I numbered each client statement (S1–S10) and linked it to requirements (FR/NFR), business rules (BR), user stories (US), prototype screens (SCR), and test focus. This makes it easy to check that nothing in the brief was left out and to assess the impact of changes.

**Business rules are data, not code.** The rule "products A and C cannot be applied to the same well" is modelled as an *incompatibility pair*, and the limit of 3 products, the 20% level, and alert thresholds are configurable parameters. New sites or clients will likely bring new rules.

**Calculations are specified, not just described.** The injection rate, the consumption estimate per well, and the autonomy have formulas, edge cases (refills, stale data, zero production, tank without associations), and a worked example that can become an automated test.

**Field users first.** Because technicians cannot install software, the system is browser-based, and the prototype is designed for tablet use, with the association flow limited to a few clicks and with rule errors that explain *why* an action is blocked.

**Methodology.** I recommend Scrum with a Sprint 0 for the implementation, and a sequential approach for the specification itself. Prioritization uses MoSCoW to define the MVP and WSJF to order the backlog, with dependencies overriding the score. The WSJF scores, KPI targets, and velocity are a **simulation** and would be calibrated with the Product Owner and the team.

**Points I would raise with the client early:**
- The diagram seems to show products A and C reaching the same well, which conflicts with the stated rule (OQ-03).
- Units of well production and tank volume, and how refills are reported by the real-time system (OQ-06, OQ-09).
- Whether a tank always contains exactly one product and whether the same product from two tanks counts once toward the limit of 3 (OQ-01, OQ-02).

---

## 3. Tools

**Used in this challenge**
- Microsoft Word (.docx) for documents and PDF for the prototype
- Python (matplotlib) for the data model diagram
- HTML/CSS rendered to PDF for the low-fidelity wireframes
- [AI assistant used to help structure and draft the material – confirm and keep this line only if it reflects how you worked; see note at the end]
- GitHub for versioning and delivery

**Tools I would use in a real project**

| Purpose | Tools |
|---------|-------|
| Requirements and backlog | Jira or Azure Boards (epics, stories, links for traceability) |
| Documentation | Confluence or SharePoint; Word/Excel for formal deliverables |
| Process and UML diagrams | draw.io / Lucidchart / Bizagi (BPMN), PlantUML or Mermaid (UML) |
| Low-fidelity prototypes | Balsamiq, Figma or Miro |
| Elicitation | Interviews, workshops and shadowing; Miro for collaborative sessions |
| Integration analysis | Postman and sample data files for the real-time system interface |
| Data analysis | Excel / SQL / Python to profile real-time data (gaps, refills, units) |
| Product metrics | Power BI or Grafana, plus product analytics for adoption KPIs |
| Communication | Teams / Slack, recorded review sessions |

---

## 4. My experience with this challenge

[Write this part in your own words. Below is a draft structure to adapt; replace anything that does not reflect what you really felt.]

- **What I liked:** The challenge is realistic. It mixes a physical process, business rules, an integration, and different user profiles, and asks for both specification and a view of delivery (methodology, prioritization, KPIs). I enjoyed turning a short brief into calculable rules and testing them with a worked example.
- **What was difficult/ambiguous:** Some points were not clear (units, the A/C conflict in the diagram, refill reporting). In a real project, I would clarify these in a session with the client, so I documented them as open questions and explicit assumptions.
- **What I would do with more time:** Validate the prototype with real users, detail the real-time integration contract and the BPMN/UML diagrams, and create a clickable mid-fidelity prototype.
- **Feedback on the challenge:** [Optional suggestions. Examples: provide a short example of the real-time data, clarify expected delivery channel (GitHub link or e-mail attachment), and indicate whether the diagram inconsistency is intentional.]
- **Time spent:** [approximately X hours]

---

## 5. Contact

Amanda Evangelista Lima · amandaelima1@gmail.com · [https://www.linkedin.com/in/amanda-evangelista-lima-3056b11aa/?isSelfProfile=true]

Thank you for the opportunity. I'm happy to walk through any of the decisions in a conversation.
