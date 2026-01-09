---
title: Quality Management & Planning
parent: Quality Planning
nav_order: 1
layout: default
---

# Quality Management & Planning Overview

A Quality Plan documents decisions about how quality will be achieved in a software project. This page introduces the four components of quality management and the key decisions that must be documented.

## Why Quality Plans Matter

> "Why do we put emphasis on a quality plan? Because in most situations quality is an afterthought." {% cite wallace1989verification %}

The more development and quality roles are combined, the more important it is to build checks and balances into the plan to ensure quality activities are not "easily tossed aside as deadlines loom."

## Four Components of Quality Management

| Component | Purpose |
|-----------|---------|
| **Quality Planning** | Identify required activities, tools, training; organize execution |
| **Quality Assurance** | Activities to provide confidence that a product *will* fulfill requirements |
| **Quality Control** | Activities to verify that a product *is* of required quality |
| **Quality Improvement** | Enhancement of process effectiveness and efficiency |

## 11 Decisions in a Quality Plan

A Quality Plan documents the following decisions:

1. **Activities** — QA, QC, and improvement activities to be conducted
2. **Interactions** — Between quality activities and development activities
3. **Artifacts** — Which work products will activities apply to
4. **Timing** — When activities will occur
5. **Responsibility** — Who performs each activity
6. **Extent** — To what depth/breadth
7. **Cost/Time** — Up-front and recurring costs
8. **Tools** — Required tooling
9. **Training** — Required skills and training
10. **Defect Handling** — How defects are reported, tracked, resolved
11. **Measurements** — Metrics providing visibility into processes

## Quality Planning Process

The quality planning process follows five steps:

```
┌─────────────────┐     ┌─────────────────────┐
│ 1. Determine    │────▶│ 2. Estimate effort  │
│    what to do   │     │    and lead times   │
└────────┬────────┘     └──────────┬──────────┘
         │                         │
         ▼                         ▼
┌─────────────────┐     ┌─────────────────────┐
│ 4. Organize     │◀────│ 3. Coordinate with  │
│    activities   │     │    development plan │
└────────┬────────┘     └─────────────────────┘
         │
         ▼
┌─────────────────┐
│ 5. Document     │
│    the plan     │
└─────────────────┘
```

## Cost of Quality

Quality costs fall into two categories {% cite wallace1989verification %}:

| Category | Type | Description |
|----------|------|-------------|
| **Conformance** | Prevention | Activities to prevent defects |
| | Appraisal | Activities to detect defects |
| **Nonconformance** | Internal failure | Defects found before delivery |
| | External failure | Defects found after delivery |
| | Effects | Lost sales, penalties, reputation |

The goal is to find the optimal balance: "How much am I willing to pay for quality?"

## Key Drivers

What determines what quality activities are needed?

1. **Process, Regulations & Standards** — External requirements
2. **Deliverables and Work Products** — User perspective (requirements, features) and producer perspective (modules, documents)
3. **Cost of Quality** — Economic trade-offs
4. **Criticality** — Impact of failure on users and producers

---

### References

{% bibliography --cited %}

---

{: .highlight }
**Disclaimer:** AI is used for text summarization, polishing and explaining. Authors have verified all facts and claims. In case of an error, feel free to file an issue.
