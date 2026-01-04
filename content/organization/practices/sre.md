---
title: Site Reliability Engineering
parent: Industry Practices
nav_order: 3
layout: default
---

# Site Reliability Engineering (SRE)

> **Reading time:** 7 min | **Level:** Intermediate

Site Reliability Engineering is an approach to operations created at Google that applies software engineering principles to infrastructure and operations problems.

---

## What is SRE?

**Google's definition:** "SRE is what happens when you ask a software engineer to design an operations team."

SRE combines:
- **Development** — writing code for automation
- **Operations** — maintaining production systems
- **Quality** — ensuring reliability and performance

### SRE vs DevOps vs Traditional Ops

| Aspect | Traditional Ops | DevOps | SRE |
|--------|-----------------|--------|-----|
| Focus | Stability | Speed + Stability | Reliability via engineering |
| Approach | Manual, reactive | Automation, collaboration | Automation + Error Budgets |
| Metrics | Uptime | Deployment frequency | SLI/SLO/SLA |
| Culture | Silos | Shared ownership | Engineering ownership |

**Key insight:** DevOps is a philosophy; SRE is a concrete implementation of that philosophy.

---

## Core Concepts

### SLI / SLO / SLA

**SLI (Service Level Indicator)** — a measurable metric of service quality:
- Availability: % of successful requests
- Latency: p50, p95, p99 response time
- Throughput: requests per second
- Error rate: % of failed requests

**SLO (Service Level Objective)** — target value for an SLI:
- "99.9% of requests succeed over 30 days"
- "p99 latency < 200ms"
- Internal team target

**SLA (Service Level Agreement)** — contract with customers:
- SLO + consequences for violation
- Usually less strict than SLO
- Legal/financial obligations

```
Example:
SLI: Availability (successful requests / total requests)
SLO: 99.95% over 30 days (internal target)
SLA: 99.9% per month (contract, penalties if breached)
```

### Error Budget

**Error Budget** = allowed amount of unreliability, derived from SLO.

```
SLO = 99.9% availability
Error Budget = 100% - 99.9% = 0.1%

Per month (30 days × 24h × 60min = 43,200 minutes):
Error Budget = 43,200 × 0.001 = 43.2 minutes of downtime allowed
```

**Using Error Budget:**

| Budget Status | Action |
|---------------|--------|
| Budget remaining | Ship new features, experiment |
| Budget exhausted | Focus on reliability, slow down releases |
| Budget negative | Stop all non-critical changes |

Error budgets align development and operations: both teams share the same goal.

---

## Toil and Automation

### What is Toil?

**Toil** = manual, repetitive, automatable work that scales linearly with service size.

Characteristics of toil:
- Manual (human intervention required)
- Repetitive (done over and over)
- Automatable (could be scripted)
- Tactical (interrupt-driven)
- No lasting value (doesn't improve the system)
- Scales with service growth

**Google's target:** SREs should spend ≤50% time on toil, ≥50% on engineering.

### Automation Priority

Prioritize automation by:
1. **Frequency** — how often is this done?
2. **Time per occurrence** — how long does it take?
3. **Risk** — what happens if done wrong?

```
Automation ROI = (Time saved per occurrence × Frequency) - Development time
```

---

## Incident Management

### Incident Response

SRE incident management principles:

1. **Detect** — monitoring and alerting
2. **Respond** — on-call rotation, escalation
3. **Mitigate** — restore service first
4. **Resolve** — fix root cause
5. **Learn** — postmortem

### Blameless Postmortems

**Goal:** Learn from incidents without blame.

Postmortem components:
- **Timeline** — what happened, when
- **Impact** — users affected, duration
- **Root cause** — why it happened
- **Action items** — how to prevent recurrence
- **Lessons learned** — what we learned

**Key principle:** Assume people acted with best intentions given available information.

---

## Monitoring and Alerting

### The Four Golden Signals

Monitor these four metrics for any service:

| Signal | Description | Example |
|--------|-------------|---------|
| **Latency** | Time to serve a request | p99 response time |
| **Traffic** | Demand on the system | Requests per second |
| **Errors** | Rate of failed requests | HTTP 5xx rate |
| **Saturation** | How "full" the service is | CPU, memory usage |

### Alerting Philosophy

Good alerts are:
- **Actionable** — requires human intervention
- **Urgent** — needs immediate attention
- **Symptomatic** — alerts on user impact, not causes

Avoid:
- Alert fatigue (too many alerts)
- Paging for non-urgent issues
- Alerts without runbooks

---

## SRE Practices Summary

| Practice | Description |
|----------|-------------|
| SLIs/SLOs | Define and measure reliability targets |
| Error Budgets | Balance reliability vs velocity |
| Toil Reduction | Automate repetitive work |
| Blameless Postmortems | Learn from failures |
| Capacity Planning | Plan for growth |
| Change Management | Controlled rollouts |

---

## Practical Application

### When to Apply SRE

SRE is most valuable when:
- Services have defined users and reliability requirements
- Scale requires automation
- Development velocity creates operational burden
- Reliability is a competitive advantage

### Starting with SRE

1. **Define SLIs** — What metrics matter to users?
2. **Set SLOs** — What reliability level is appropriate?
3. **Measure** — Implement monitoring
4. **Calculate Error Budget** — Track remaining budget
5. **Reduce Toil** — Automate repetitive tasks
6. **Learn from Incidents** — Implement postmortems

---

## Related Topics

- [Reliability Strategies](../../attributes/reliability/) — Fault tolerance, redundancy
- [Performance Testing](../../attributes/performance/) — Load testing, benchmarking
- [CI/CD Quality Gates](../project-quality/quality-planning/) — Automated quality checks

---

## Further Reading

- [Site Reliability Engineering](https://sre.google/sre-book/table-of-contents/) — Google (free online)
- [The Site Reliability Workbook](https://sre.google/workbook/table-of-contents/) — Google (free online)
- [Building Secure & Reliable Systems](https://sre.google/books/) — Google (free online)
- "Implementing Service Level Objectives" — Alex Hidalgo (O'Reilly, 2020)
- [Google SRE Resources](https://sre.google/resources/)

---

{: .note }
SRE originated at Google but principles apply to organizations of any size. Start small with SLIs/SLOs and expand practices as needed.

---

{: .highlight }
**Disclaimer:** AI is used for text polishing and explaining. Authors have verified all facts and claims. In case of an error, feel free to file an issue.
