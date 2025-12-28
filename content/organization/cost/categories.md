---
title: Cost Categories
parent: Cost of Quality
nav_order: 1
layout: default
---

# Cost of Quality Categories

The Cost of Quality framework classifies all quality-related costs into four categories: Prevention, Appraisal, Internal Failure, and External Failure.

---

## The Four Categories

### 1. Prevention Costs

Costs incurred to prevent defects from occurring.

**Examples**:
- Quality planning activities
- Requirements reviews
- Design reviews
- Code reviews and inspections
- Test planning
- Process improvement initiatives
- Training and skill development
- Tool acquisition (linters, static analyzers)
- Standards development
- Root cause analysis

**Typical percentage**: 5-10% of total COQ

### 2. Appraisal Costs

Costs of measuring, evaluating, and auditing quality.

**Examples**:
- Test execution (unit, integration, system)
- Code coverage analysis
- Static code analysis
- Security scanning
- Performance testing
- Usability testing
- Quality audits
- Reviews and inspections (time spent)
- Test environment maintenance
- Test data preparation

**Typical percentage**: 20-25% of total COQ

### 3. Internal Failure Costs

Costs of defects found before delivery to customers.

**Examples**:
- Debugging and defect fixing
- Rework and redesign
- Retesting after fixes
- Regression testing
- Scrap (discarded code)
- Downtime due to defects
- Test environment issues
- Build failures
- Deployment rollbacks

**Typical percentage**: 25-40% of total COQ

### 4. External Failure Costs

Costs of defects found after delivery to customers.

**Examples**:
- Customer support for defect-related issues
- Emergency patches and hotfixes
- Warranty claims
- Product recalls
- Liability and legal costs
- Lost sales due to reputation damage
- Customer dissatisfaction
- Service level agreement (SLA) penalties
- Production incident response
- Data breach remediation

**Typical percentage**: Can be 40-50%+ of total COQ in poor-quality organizations

---

## Cost Category Relationships

### Prevention vs. Failure

```
↑ Prevention → ↓ Failures
↓ Prevention → ↑ Failures (especially external)
```

Optimal strategy: Maximize prevention, minimize failures.

### The PAF Model

Prevention-Appraisal-Failure model:

- **Increase Prevention** → Reduce Internal + External Failures
- **Increase Appraisal** → Shift External Failures to Internal
- **Reduce Failures** → Lower Total COQ

---

## Cost Distribution Patterns

### Poor Quality Organization

- Prevention: 5%
- Appraisal: 10%
- Internal Failure: 35%
- External Failure: 50%

High total costs, mostly spent on failures.

### Average Quality Organization

- Prevention: 10%
- Appraisal: 25%
- Internal Failure: 40%
- External Failure: 25%

Moderate costs, still significant failure costs.

### World-Class Quality Organization

- Prevention: 40%
- Appraisal: 30%
- Internal Failure: 25%
- External Failure: 5%

Lower total costs, invested in prevention.

---

## Collecting Category Data

### Prevention Cost Data

Sources:
- Time tracking (reviews, planning)
- Training budgets
- Tool licenses
- Process improvement project costs

### Appraisal Cost Data

Sources:
- Testing effort from time sheets
- QA team salaries allocated to testing
- Test tool and infrastructure costs
- Audit costs

### Internal Failure Cost Data

Sources:
- Time spent on rework
- Defect fixing effort
- Build and deployment failures
- Test environment issues

### External Failure Cost Data

Sources:
- Customer support tickets (defect-related)
- Hotfix development effort
- SLA penalty payments
- Customer churn analysis

---

## Using Category Analysis

### Identify Improvement Opportunities

High external failure costs? → Invest in testing (appraisal) and prevention

High internal failure costs? → Improve prevention (reviews, training)

Low prevention costs? → Likely opportunity to reduce total COQ

### Track Improvement

Monitor category distribution over time:
- Are prevention costs increasing?
- Are failure costs decreasing?
- Is total COQ trending down?

### Benchmark

Compare to industry standards:
- Similar product types
- Comparable maturity levels
- Best-in-class organizations

---

{: .note }
**Status**: Placeholder. Detailed content with calculation examples, data collection templates, and case studies will be added.

---

{: .highlight }
**Disclaimer:** AI is used for text polishing and explaining. Authors have verified all facts and claims. In case of an error, feel free to file an issue.
