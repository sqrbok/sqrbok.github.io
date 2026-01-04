---
title: Industry Practices
parent: Organizing Quality
nav_order: 5
layout: default
has_children: true
---

# Industry Practices

This section examines how leading technology companies approach software quality at scale. These practices have been refined through years of experience and have influenced the broader industry.

---

## Overview

Large technology companies face unique quality challenges:
- Millions of users depending on services
- Thousands of engineers contributing code
- Rapid release cycles (multiple deploys per day)
- Complex distributed systems

Their solutions provide valuable lessons for organizations of any size.

---

## Topics in This Section

### [Google Engineering Practices](google.md)

How Google maintains quality across 2+ billion lines of code:
- Code review at scale (every change reviewed)
- Testing philosophy and the test pyramid
- Monorepo benefits and quality implications
- Release engineering and safe deployments
- Postmortem culture and blameless learning

### [Microsoft Quality Practices](microsoft.md)

Microsoft's evolution from packaged software to cloud services:
- Security Development Lifecycle (SDL)
- One Engineering System (1ES)
- Feature flags and ring-based deployment
- Shift-left testing philosophy
- Telemetry-driven quality decisions

### [Site Reliability Engineering (SRE)](sre.md)

Google's approach to operations as engineering:
- SLI / SLO / SLA framework for reliability targets
- Error budgets for balancing reliability and velocity
- Toil reduction and automation focus
- Incident management and on-call practices
- Blameless postmortems for organizational learning

---

## Common Themes

Despite different origins, these practices share common principles:

| Principle | Google | Microsoft | SRE |
|-----------|--------|-----------|-----|
| **Automation** | Automated testing, CI/CD | 1ES pipelines | Toil elimination |
| **Measurement** | Metrics-driven decisions | Telemetry | SLIs/SLOs |
| **Gradual rollout** | Canary releases | Ring deployment | Error budgets |
| **Learning from failure** | Postmortems | Incident reviews | Blameless culture |
| **Shift left** | Early testing, code review | SDL integration | Proactive reliability |
| **Ownership** | Developer owns quality | Combined engineering | Engineering owns ops |

---

## Key Concepts

### Code Review at Scale

Both Google and Microsoft review every code change:
- **Purpose**: Catch issues early, share knowledge, maintain standards
- **Speed**: Aim for <24 hour turnaround
- **Culture**: Constructive feedback, no gatekeeping
- **Tooling**: Automated checks before human review

### The Test Pyramid

Industry-standard testing distribution:

```
        /\
       /  \      E2E Tests (10%)
      /----\     - Slow, expensive, catch integration issues
     /      \    
    /--------\   Integration Tests (20%)
   /          \  - Test component interactions
  /------------\ 
 /              \ Unit Tests (70%)
/----------------\ - Fast, isolated, verify logic
```

### Service Level Objectives (SLOs)

Defining and measuring reliability:
- **SLI** (Service Level Indicator): What we measure (availability, latency)
- **SLO** (Service Level Objective): Target value (99.9% availability)
- **SLA** (Service Level Agreement): Contract with consequences

### Error Budgets

Balancing reliability and innovation:
```
Error Budget = 100% - SLO

Example: 99.9% SLO = 0.1% error budget = 43 minutes/month downtime allowed

Budget available → Ship features, experiment
Budget exhausted → Focus on reliability
```

### Safe Deployment

Gradual rollout strategies:
1. **Canary**: Deploy to small % of traffic first
2. **Rings**: Expand through dev → internal → early adopters → all
3. **Feature flags**: Separate deploy from release
4. **Auto-rollback**: Revert on error spike

### Blameless Postmortems

Learning from incidents without blame:
- Focus on **systems**, not individuals
- Document timeline, impact, root cause
- Define action items with owners
- Share learnings broadly

---

## Applying Industry Practices

### What Scales Down

These practices work at any organization size:

| Practice | Implementation |
|----------|----------------|
| Code review | Every PR reviewed before merge |
| Automated testing | CI runs tests on every commit |
| SLOs | Define availability targets, measure them |
| Postmortems | Document and learn from incidents |
| Gradual rollout | Even manual staged deployments help |

### What Requires Investment

These need significant tooling or team size:

| Practice | Investment Required |
|----------|---------------------|
| Monorepo | Sophisticated build and test infrastructure |
| Feature flags at scale | Feature management platform |
| Dedicated SRE team | Headcount, on-call rotation |
| Readability process | Critical mass of certified reviewers |
| Ring deployment | Multiple environments, automation |

### Getting Started

Recommended adoption sequence:

1. **Culture first** — Blameless reviews, quality ownership
2. **Automation** — CI/CD, automated testing
3. **Measurement** — Define and track SLOs
4. **Gradual rollout** — Feature flags, staged deployments
5. **Maturity** — Formal postmortems, capacity planning

---

## Comparison with Traditional Approaches

| Aspect | Traditional | Industry Practices |
|--------|-------------|-------------------|
| Quality responsibility | QA team | Everyone |
| Deployment frequency | Monthly/quarterly | Daily/continuous |
| Incident response | Blame and fix | Learn and improve |
| Testing | Phase at end | Continuous throughout |
| Reliability target | "As high as possible" | Specific SLO |

---

## Further Reading

### Books (Free Online)
- [Site Reliability Engineering](https://sre.google/sre-book/table-of-contents/) — Google
- [The Site Reliability Workbook](https://sre.google/workbook/table-of-contents/) — Google
- [Software Engineering at Google](https://abseil.io/resources/swe-book/html/toc.html) — O'Reilly

### Documentation
- [Google Engineering Practices](https://google.github.io/eng-practices/) — Code review guide
- [Microsoft SDL](https://www.microsoft.com/en-us/securityengineering/sdl) — Security Development Lifecycle
- [Google Style Guides](https://google.github.io/styleguide/)

### Additional Reading
- "The DevOps Handbook" — Kim, Humble, Debois, Willis
- "Accelerate" — Forsgren, Humble, Kim
- "Implementing Service Level Objectives" — Alex Hidalgo

---

## Related Topics

- [CMMI](../standards/cmmi/) — Process maturity framework
- [Process Improvement](../processes/improvement/) — PDCA, DMAIC
- [Quality Planning](../project/planning/) — Project-level quality management

---

{: .note }
Industry practices continue to evolve. What works for Google or Microsoft may need adaptation for your context. Focus on principles over specific implementations.

---

{: .highlight }
**Disclaimer:** AI is used for text polishing and explaining. Authors have verified all facts and claims. In case of an error, feel free to file an issue.
