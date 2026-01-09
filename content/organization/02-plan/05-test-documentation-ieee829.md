---
title: Test Documentation (IEEE 829)
parent: Quality Planning
nav_order: 5
layout: default
---

# Test Documentation (IEEE 829)

IEEE 829-2008 provides the standard structure for software test documentation. This page covers the Master Test Plan structure, tailoring guidelines, and the "addressed" principle.

## Master Test Plan Structure

The Master Test Plan (MTP) provides the overarching test management structure {% cite ieee829-2008 %}:

### Part 1: Introduction

| Section | Content |
|---------|---------|
| **Identifier** | Unique document identifier |
| **Scope** | What is and isn't covered |
| **References** | Related documents |
| **System Overview** | High-level description of system under test |
| **Test Overview** | Schedule, resources, responsibilities, tools/methods |

### Part 2: Details

| Section | Content |
|---------|---------|
| **Test Processes** | How testing will be conducted |
| **Test Levels** | Component, integration, system, acceptance |
| **Documentation Requirements** | What documents will be produced |
| **Administration** | How testing will be managed |
| **Reporting** | How results will be communicated |

### Part 3: General

| Section | Content |
|---------|---------|
| **Glossary** | Definitions of terms |
| **Change Procedures** | How plan changes are handled |
| **Version History** | Document revision history |

## Level Test Plans

Each test level (component, integration, system, acceptance) has its own Level Test Plan (LTP) containing:

1. **Test Items** — What will be tested
2. **Features to Test** — Specific features covered
3. **Features Not to Test** — Excluded features with rationale
4. **Approach** — Testing techniques and methods
5. **Pass/Fail Criteria** — How success is determined
6. **Suspension/Resumption Criteria** — When to pause/restart
7. **Environmental Needs** — Hardware, software, tools required

## The "Addressed" Principle

> All topics must be formally decided: include, record in tool, or exclude with rationale. {% cite ieee829-2008 %}

For each required topic, you must:

| Option | Meaning |
|--------|---------|
| **Include** | Document the information in the plan |
| **Record in Tool** | Reference where information is stored (e.g., in test management tool) |
| **Exclude with Rationale** | Explicitly state why not applicable |

**Never leave topics unaddressed.**

## Integrity-Level Mapping

Documentation depth should be commensurate with criticality {% cite ieee829-2008 %}:

| Integrity Level | Documentation Depth |
|----------------|---------------------|
| High (safety-critical) | Full documentation, formal reviews |
| Medium | Standard documentation |
| Low | Abbreviated documentation allowed |

## Tailoring Guidelines

**Combine documents** when:
- Project is small
- Single test level
- Resources limited

**Separate documents** when:
- Project is complex
- Multiple teams involved
- Regulatory requirements

**Reference existing data:**
- Avoid duplication by referencing PM plans, QA plans
- Use hyperlinks to related documents

## IEEE 829 Outline

Standard test plan sections:

1. Test Plan Identifier
2. Table of Contents
3. References
4. Glossary
5. Introduction
6. Test Items
7. Software Risk Issues
8. Features to Be Tested
9. Features Not to Be Tested
10. Approach
11. Item Pass/Fail Criteria
12. Suspension Criteria and Resumption Requirements
13. Test Deliverables
14. Testing Tasks
15. Environmental Needs
16. Responsibilities
17. Staffing and Training Needs
18. Schedule
19. Planning Risks and Contingencies
20. Approvals

## Iterative Updates

> Update plans when requirements change. {% cite ieee829-2008 %}

Test documentation is living documentation:
- Review at each milestone
- Update when scope changes
- Re-baseline after major changes
- Track version history

---

### References

{% bibliography --cited %}

---

{: .highlight }
**Disclaimer:** AI is used for text summarization, polishing and explaining. Authors have verified all facts and claims. In case of an error, feel free to file an issue.
