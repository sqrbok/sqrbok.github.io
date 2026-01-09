---
title: V&V Activities & Process Models
parent: Quality Planning
nav_order: 2
layout: default
---

# V&V Activities & Process Models

Verification and Validation (V&V) activities ensure software quality is built-in during each phase of development. This page covers the minimum V&V tasks by phase and testing process models for organizing these activities.

## V&V Activities by SDLC Phase

Wallace 1989 defines minimum V&V tasks that should be performed during each software development phase {% cite wallace1989verification %}:

### Requirements Phase

| Task | Focus |
|------|-------|
| **Traceability Analysis** | Trace requirements back to system concept |
| **Requirements Validation** | Correctness, consistency, completeness, accuracy, readability, testability |
| **Interface Analysis** | Hardware, software, and operator interfaces |
| **System Test Planning** | Begin planning for compliance with functional requirements |
| **Acceptance Test Planning** | Begin planning for acceptance requirements |

### Design Phase

| Task | Focus |
|------|-------|
| **Traceability Analysis** | Trace design back to requirements |
| **Design Evaluation** | Correctness, consistency, design quality |
| **Interface Analysis** | Data items and performance at boundaries |
| **Component Test Planning** | Plan for design compliance, timing, accuracy |
| **Integration Test Planning** | Plan for functional requirements at stress limits |

### Implementation Phase

| Task | Focus |
|------|-------|
| **Traceability Analysis** | Trace source code to design |
| **Code Evaluation** | Correctness, code quality |
| **Interface Analysis** | Data/control access across interfaces |
| **Component Test Execution** | Verify component integrity |

### Test Phase

| Task | Focus |
|------|-------|
| **Integration Test Execution** | Subsystem elements and interface requirements |
| **System Test Execution** | Entire system at limits and stress conditions |
| **Acceptance Test Execution** | Performance with operational scenarios |

## Testing Process Models

A systematic review identified 17 testing process models, most defining 5 maturity levels {% cite hrabovska2019testing %}:

| Model | Structure |
|-------|-----------|
| **TMM** | Initial → Definition → Integration → Management/Measurement → Optimization |
| **TMMi** | Initial → Managed → Defined → Measured → Optimization |
| **TPI** | 20 Key Areas with 4 maturity levels each |
| **ISO/IEC/IEEE 29119** | Organizational → Test Management → Dynamic Test Processes |
| **TIM** | Initial → Baselining → Cost-effectiveness → Risk-lowering → Optimizing |

### Five Testing Phases

Most models structure testing activities through five phases:

1. **Planning** — Define objectives, scope, approach, schedule
2. **Test Case Design** — Create test cases from requirements/specifications
3. **Setup** — Prepare test environment and data
4. **Execution/Evaluation** — Run tests and evaluate results
5. **Monitoring/Control** — Track progress and manage deviations

## Early V&V in Model-Based Systems Engineering

For MBSE contexts, early V&V checks system design quality before concrete realization {% cite cederbladh2023vv %}:

| Technique | Description |
|-----------|-------------|
| **Simulation** | Model execution, "virtual testing," co-simulation |
| **Model Checking** | Formal verification (deadlock, liveness proofs) |
| **Manual Review** | Engineering reviews applied to models |
| **Static Analysis** | Program analysis without full execution |
| **Model Transformations** | Automated conversion between modeling languages (63% of studies) |

**Quality Plan Incorporation:**
- Treat models as primary artifacts (not just documents)
- Define tooling (Cameo, MagicDraw, Simulink) and interoperability
- Quality gates for models (e.g., deadlock-freeness before implementation)

## Agile and Quality Assurance

A common misconception: "I am using an agile approach so my plan does not require quality assurance activities."

Philip Koopman's critique (2010) {% cite koopman2010agile %}:

> "Without an external check and balance it is all too easy to have a process failure."

### The Trust Problem

Koopman argues that Agile relies on a "trust picture" where developers are expected to do the right thing—often at the expense of external audits and objective verification:

| Risk | Description |
|------|-------------|
| **Lack of External Oversight** | No independent verification mechanisms |
| **Subjectivity of Success** | Difficult to determine if team is actually writing quality code |
| **Sustainability Risks** | Quality depends on individual "hero" leaders—high risk if they leave |
| **Auditing Gaps** | Audits are not part of typical Agile trust model |

### Three Evaluative Questions for Agile Teams

1. "Show me the written process you are following" (format can be flexible)
2. "Explain to me how an external person can tell whether you are actually following that process"
3. "Explain to me how an external person can tell that the process is producing the quality of software you want"

**Quality Plan implication:** Even Agile teams need defined processes combined with independent quality verification.

---

### References

{% bibliography --cited %}

---

{: .highlight }
**Disclaimer:** AI is used for text summarization, polishing and explaining. Authors have verified all facts and claims. In case of an error, feel free to file an issue.
