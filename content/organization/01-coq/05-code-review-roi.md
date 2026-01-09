---
title: Code Review ROI
parent: Cost of Quality
nav_order: 5
layout: default
---

# Code Review ROI

The Return on Investment (ROI) of code review is significantly influenced by how participants prioritize high-value findings, manage potential debt, and provide actionable guidance to minimize rework costs {% cite turzo2023useful %} {% cite fu2022ptd %}.

## Code Review Usefulness Factors

Research into the OpenDev community by Turzo & Bosu (2023) identifies several technical and non-technical factors that determine if a review is perceived as useful by developers, who typically spend **10–15% of their time** on review tasks {% cite turzo2023useful %}:

### Key Usefulness Criteria

| Factor | % Respondents |
|--------|---------------|
| **Finds defects** | 44.4% |
| **Improves code quality** | 42.5% |
| Uses appropriate language | 28.1% |
| **Maintainability** | 28.1% |
| Facilitates knowledge sharing | 25.0% |

### Linguistic Characteristics

**Surprising finding:** ~28% of developers judge usefulness based on **how feedback is communicated**—specifically looking for {% cite turzo2023useful %}:
- Constructive criticism
- Respectful tone
- Clear, concrete examples

### Participant Factors

| Factor | Impact on Usefulness |
|--------|---------------------|
| Reviewer coding experience | **Positive** association |
| Mutual "quid pro quo" reviews | **Negative** association |

## The "Usefulness Gap" Problem

A major challenge to CR ROI is the high volume of low-value feedback, with **20–44% of reviews** often being marked as "not useful" by authors {% cite turzo2023useful %}:

### Comment Distribution

| Comment Category | % of Comments | Avg. Usefulness |
|------------------|---------------|-----------------|
| **Functional Defect** | <20% | Highest (4.38/5) |
| Documentation | 33.32% | Medium (3.73/5) |
| Visual/Styling | 3.92% | **Lowest** (2.92/5) |

### The "Shallow Review" Trap

Large code changes (high churn) often lead to shallow reviews where reviewers opt for easy "Documentation" comments rather than the high-effort task of finding functional defects {% cite turzo2023useful %}.

**Key insight:** Most effort goes to low-value comments; **<20% address functional defects**.

## Security Defects in Code Review

Yu et al. (2023) studied the OpenStack and Qt communities to determine how effectively human reviewers catch security issues {% cite yu2023security %}:

### Study Parameters

| Metric | Value |
|--------|-------|
| Total comments analyzed | 432,585 |
| Security-related comments | 614 (<1%) |
| Communities | OpenStack, Qt |

### Top Security Defect Types Found

| Defect Type | % of Security Issues |
|-------------|---------------------|
| **Race Conditions** | 39.0% |
| **Crashes** | 22.8% |
| **Resource Leaks** | 10.9% |

### Resolution Rates

| Condition | Fix Rate |
|-----------|----------|
| Overall | 65.9% |
| **With specific solution** | **81.3%** |
| Without guidance | 59.5% |

**Key insight:** Providing specific solutions increases fix rate by **22 percentage points** {% cite yu2023security %}.

### The 30% Escape Problem

Even when identified, ~30% of security defects remain unresolved due to:
- "Not worth fixing now" (45.4%)
- Developer-reviewer disagreement (34.0%)

## Potential Technical Debt (PTD) Detection

Fu et al. (2022) defined Potential Technical Debt (PTD) as sub-optimal implementations identified during review that can be resolved **before** being merged into the codebase {% cite fu2022ptd %}:

### PTD Prevalence

| Metric | Value |
|--------|-------|
| Comments containing PTD | ~8.0% |
| PTD identified by reviewers | **87.7%** |
| Developers unaware of their PTD | ~88% |

### PTD Types and Resolution Rates

| PTD Type | % of Total PTD | Resolution Rate |
|----------|----------------|-----------------|
| **Code PTD** | 33.7% | 89.1% |
| **Documentation PTD** | 27.6% | 86.7% |
| **Test PTD** | 12.9% | **90.5%** |
| **Design PTD** | 12.3% | 80.0% |
| **Requirement PTD** | 7.4% | **16.7%** (problematic) |

**Average resolution:** 81% of PTD resolved during review; **19% escapes to become actual TD** {% cite fu2022ptd %}.

### Requirement PTD Challenge

Requirement PTD has the lowest resolution rate (16.7%) because it often depends on:
- External stakeholder decisions
- Future sprints/releases
- Budget constraints

## ROI Optimization Recommendations

To maximize the value of code reviews, organizations should move away from "checkbox" compliance toward a data-informed approach {% cite turzo2023useful %} {% cite bakhtiary2020tdd %}:

### Practice Recommendations

| Practice | Expected Impact |
|----------|-----------------|
| **Rotate reviewers** | Avoids quid pro quo pairs |
| **Assign experienced reviewers to critical code** | +Functional defect detection |
| **Keep changesets small** | +Thorough reviews |
| **Provide specific solutions** | +22% fix rate for security issues |
| **Track unresolved PTD explicitly** | Prevents TD accumulation |

### Shift to Prevention

Implementing Test-Driven Development (TDD) can reduce pre-release defects by **61–62%**, significantly lowering the appraisal burden during code review {% cite bakhtiary2020tdd %}.

## Economic Model

### PTD Resolution Cost Example

| Timing | Cost per Issue | Multiplier |
|--------|----------------|------------|
| During review (context fresh) | ~$50 | 1× |
| After merge (as TD) | ~$500 | 10× |

**Code review ROI:** ~73% reduction in total remediation costs when PTD is caught early {% cite fu2022ptd %}.

### ROI Summary

| Metric | Value |
|--------|-------|
| Developer time on reviews | 10–15% |
| Reviews marked "not useful" | 20–44% |
| PTD caught by reviewers | 87.7% |
| Security fix rate with guidance | 81.3% |
| Cost multiplier (TD after merge) | 10× |

---

### References

{% bibliography --cited %}

---

{: .highlight }
**Disclaimer:** AI is used for text summarization, polishing and explaining. Authors have verified all facts and claims. In case of an error, feel free to file an issue.
