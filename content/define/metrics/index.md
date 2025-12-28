---
title: Metrics
nav_order: 4
parent: Quality
layout: default
has_children: true
---

# Quality Metrics

**"You can't improve what you don't measure."** - Peter Drucker

Quality metrics provide quantitative measures that help us understand, monitor, and improve software quality. But not all metrics are created equal—choosing the right metrics and using them correctly is critical.

---

## Why Metrics Matter

Metrics enable:
- **Objective assessment** - Move beyond gut feelings to data-driven decisions
- **Early detection** - Identify quality issues before they become expensive
- **Process improvement** - Track progress and measure effectiveness of changes
- **Communication** - Provide concrete evidence for stakeholders
- **Prediction** - Estimate effort, defects, and maintenance costs

Without metrics, quality management becomes guesswork.

---

## Learning Objectives

This section helps you learn to:

1. **Define measurement and metrics** - Understand fundamental concepts in software quality measurement
2. **Recognize common pitfalls** - Identify and avoid measurement mistakes
3. **Evaluate measurement data** - Assess scale, precision, reliability, and validity
4. **Develop valid metrics** - Create metrics for specific quality concerns
5. **Critically assess metrics** - Evaluate new metrics for usefulness and applicability
6. **Design metrics programs** - Implement successful measurement while mitigating risks

---

## Topics in This Section

### [Definitions](definitions.md)
Understand the fundamental concepts:
- What is measurement vs. a metric?
- Direct vs. derived metrics
- Attributes, entities, and measures
- Measurement scales (nominal, ordinal, interval, ratio)

### [Measurements](measurements.md)
Learn about different categories of metrics:
- **Product metrics** - Size, complexity, quality attributes
- **Process metrics** - Efficiency, effectiveness, maturity
- **Resource metrics** - Effort, cost, schedule

### [Examples](examples.md)
Explore commonly used software metrics:
- Lines of Code (LOC)
- Cyclomatic complexity
- Defect density
- Code coverage
- Function points

### [Development](devel.md)
Learn systematic approaches to creating metrics:
- **Goal-Question-Metric (GQM)** paradigm
- Aligning metrics with business goals
- Ensuring metrics are actionable
- Validation and calibration

### [Pitfalls](ptifalls.md)
Avoid common measurement mistakes:
- Measuring the wrong things
- Gaming the metrics
- Over-reliance on a single metric
- Ignoring context
- Lack of baselines

---

## Key Principles

### 1. Measure with Purpose
Every metric should support a specific goal. Don't measure just because you can.

### 2. Keep It Simple
Complex metrics are hard to understand, calculate, and act upon. Start simple.

### 3. Metrics Drive Behavior
People optimize for what's measured. Ensure your metrics incentivize the right behaviors.

### 4. Context Matters
The same metric value can be good in one context and bad in another. Always interpret metrics in context.

### 5. Use Multiple Metrics
No single metric captures all aspects of quality. Use a balanced set.

---

## The GQM Approach

**Goal-Question-Metric** is a systematic approach to defining metrics:

1. **Goal** - What do you want to achieve?
   - Example: "Improve software reliability"

2. **Question** - What questions help assess progress toward the goal?
   - Example: "How many defects are found in production?"

3. **Metric** - What measurements answer those questions?
   - Example: "Defects per 1000 lines of code in production"

This ensures metrics are purposeful and actionable.

---

## Common Metric Categories

| Category | Examples | Purpose |
|----------|----------|---------|
| **Size** | LOC, function points | Estimate effort, normalize other metrics |
| **Complexity** | Cyclomatic complexity, nesting depth | Predict defects, guide refactoring |
| **Quality** | Defect density, reliability | Assess product quality |
| **Testing** | Code coverage, mutation score | Measure test effectiveness |
| **Process** | Defect removal efficiency | Improve development process |
| **Maintenance** | Change rate, MTTR | Track long-term costs |

---

## Avoiding Metric Abuse

**Goodhart's Law**: "When a measure becomes a target, it ceases to be a good measure."

**Warning signs:**
- Developers optimizing code to improve metrics rather than quality
- Metrics causing harmful behaviors (e.g., avoiding necessary complexity)
- Focus on metrics overshadowing actual goals
- Lack of critical thinking about what metrics mean

**Solutions:**
- Use metrics for information, not punishment
- Balance quantitative metrics with qualitative assessment
- Review and evolve your metric suite regularly
- Foster a culture of quality, not just measurement

---

## Further Reading

After mastering metrics, explore:
- [Quality Models](../models.md) - Structured frameworks for quality
- [Verification and Validation](../../verif/) - Measuring testing effectiveness
- [Quality Attributes](../../attributes/) - Metrics for specific quality characteristics

---

{: .highlight }
**Disclaimer:** AI is used for text polishing and explaining. Authors have verified all facts and claims. In case of an error, feel free to file an issue.
