---
title: Quality Gates & Criticality
parent: Quality Planning
nav_order: 3
layout: default
---

# Quality Gates & Criticality

Quality gates are predefined checkpoints that ensure software meets required criteria before progressing to the next development phase. This page covers quality gate definitions, criticality-based tailoring, and modern tooling.

## What Are Quality Gates?

Quality gates are predefined checkpoints within the SDLC positioned at various stages {% cite uzunova2024qualitygates %}:

| Definition | Description |
|------------|-------------|
| **Structured Checkpoints** | Predefined quality criteria a project must meet to move between stages |
| **Decision Points** | Critical junctures with quality-focused "go/no-go" criteria |
| **Transparency Mechanism** | Formal checklists, sign-offs, and acceptance procedures |

> "Quality gates are predefined checkpoints within the software development life-cycle." {% cite uzunova2024qualitygates %}

## Entry and Exit Criteria

IEEE 829-2008 specifies that test plans must define {% cite ieee829-2008 %}:

- **Pass/Fail Criteria** — Criteria for determining if a test item passed or failed (typically based on anomaly count/severity)
- **Suspension Criteria** — When to pause testing (e.g., defects make further testing valueless)
- **Resumption Criteria** — What must be done to restart testing

**Principle:** Define entry/exit criteria according to artifact criticality.

## Criticality Levels

### DO-178B Avionic Software Criticality

| Level | Safety Impact | Coverage Requirement |
|-------|--------------|---------------------|
| **A** | Catastrophic failure | 100% Modified Condition/Decision Coverage (MC/DC) |
| **B** | Hazardous/severe failure | 100% Decision Coverage |
| **C** | Major failure | 100% Statement Coverage |
| **D** | Minor failure | 100% Requirements Coverage |
| **E** | No adverse effect | No coverage requirements |

### Quality Gates by Criticality

| Condition | Low (C) | Medium (B) | High (A) |
|-----------|---------|------------|----------|
| Coverage | Statement | Branch | Basis paths |
| Code inspections | No | Yes | Yes |
| Coding standards | Yes | Yes | Yes |
| Testing strength | All pairs | All triples | All quadruples |
| Cyclomatic complexity | <20 | <20 | <15 |

## Phased Quality Gates (Microsoft Example)

Quality gates can be achieved progressively across milestones:

| Area | M1 | M2 | M3 | Release |
|------|----|----|----|----|
| Test execution | — | Priority 1 tests | Priority 1+2 tests | All tests |
| Code coverage | Measured | 65% | 75% | 80% |
| Stress testing | P1 nightly | 200 computers | 500 computers | 500 computers, no issues |

> "Sometimes adequacy criteria could be achieved over time."

## Quality Gate Tools

Modern tools automate quality gate enforcement {% cite uzunova2024qualitygates %}:

| Tool | Focus |
|------|-------|
| **SonarQube/SonarCloud** | Static analysis; blocks builds if bugs/coverage criteria not met |
| **Sigrid (SIG)** | Risk management, architecture, technical debt monitoring |
| **Veracode** | Security-focused static/dynamic analysis |
| **Maverix.ai** | AI-driven issue detection, real-time feedback |
| **Squore (Vector)** | Maintainability, technical debt dashboards |

## Documenting Quality Gates

For Quality Plan documentation {% cite uzunova2024qualitygates %}:

1. **Document criteria explicitly** — metric, desired value, predicate, object of measurement
2. **Use formal checklists** — Maintain transparency, ensure repeatable sign-off
3. **Set clear thresholds** — e.g., "85% code coverage" for objective evaluation
4. **Continuous refinement** — Review and update based on feedback
5. **Hybrid balance** — Combine manual processes (code reviews) with automated tools

## The Quality Triangle

Quality gates help navigate the classic trade-off:

```
        Quality
         /\
        /  \
       /    \
      /______\
   Scope    Time/Cost
```

Through phasing, quality gates implement "the good enough" approach — achieving acceptable quality within constraints.

---

### References

{% bibliography --cited %}

---

{: .highlight }
**Disclaimer:** AI is used for text summarization, polishing and explaining. Authors have verified all facts and claims. In case of an error, feel free to file an issue.
