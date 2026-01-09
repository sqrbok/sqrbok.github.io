---
title: Test Effort Estimation
parent: Quality Planning
nav_order: 4
layout: default
---

# Test Effort Estimation

Estimating test effort is challenging due to the many factors affecting testing. This page covers estimation methods, tester-to-developer ratios, and practical calculation approaches.

## Estimation Challenges

> "Test effort estimation remains challenging due to the many factors affecting testing." {% cite bluemke2021testeffort %}

**Key factors affecting test effort:**
- System size and complexity
- Tester experience
- Test environment stability
- Requirements volatility
- Defect density

## Estimation Methods

A systematic review identified multiple approaches {% cite bluemke2021testeffort %}:

| Method | Description |
|--------|-------------|
| **Test Point Analysis (TPA)** | Function point-based, accounts for test complexity |
| **Use Case Points (UCP)** | Estimates from use case specifications |
| **Machine Learning** | Neural networks, regression for prediction |
| **Expert Judgment** | Experience-based estimation |
| **Analogy** | Based on similar past projects |

## Tester-to-Developer Ratios

Ratios vary significantly by product type {% cite kaner2000measurement %}:

| Product Type | Developers | Ratio (Dev:Tester) | Testers |
|--------------|------------|-------------------|---------|
| Commercial (Large Market) | 30 | 3:2 | 20 |
| Commercial (Small Market) | 30 | 3:1 | 10 |
| Heavy COTS Integration | 30 | 4:1 | 7 |
| Government (Internal) | 30 | 5:1 | 6 |
| Corporate (Internal) | 30 | 4:1 | 7 |

**Industry range:** From 1:5 through 5:1

**Microsoft:** 1:1 ratio

## Function Point-Based Estimation

Test cases per function point by software type (Jones 2008):

| Test Type | Systems | MIS | Military | Commercial |
|-----------|---------|-----|----------|------------|
| Unit test | 0.30 | 0.20 | 0.50 | 0.30 |
| New function test | 0.35 | 0.25 | 0.35 | 0.25 |
| Regression test | 0.30 | 0.10 | 0.30 | 0.35 |
| Integration test | 0.45 | 0.25 | 0.75 | 0.35 |
| System test | 0.40 | 0.20 | 0.55 | 0.40 |
| **Total** | **1.80** | **1.00** | **2.45** | **1.65** |

**Formula:** `TotalTestCases = FunctionPoints^1.2`

*Example: 100 FP → ~251 test cases*

## Back-of-Envelope Calculations

### White Box Estimation

Number of tests for branch coverage = **n + 1** (where n = number of predicates)

- Average from SONAR database: **25% of LOC are decisions**
- Example: 1000 LOC → 250 decisions → 250 test cases

### Black Box Estimation

Test cases per function based on complexity × criticality:

| Complexity | Non-critical | Medium | Critical |
|------------|--------------|--------|----------|
| Simple (2 inputs) | 8 | 12 | 12 |
| Medium (4 inputs) | 8 | 15 | 21 |
| Complex (6 inputs) | 8 | 16 | 40 |

**Assumptions:**
- Each function may require up to 3× test cases (depending on unit/integration inclusion)
- Each input has two equivalence classes
- Number of tests depends on criticality

### Total Effort Formula

```
TotalTestCases = (1 + I + U) × Σ TestCasesPerFunction[i,j]

Where:
  1 = System level tests
  I = Fraction for integration (0 < I < 1)
  U = Fraction for unit testing (0 if under development, else 0 < U < 1)

Effort = TotalTestCases × [DesignEffort + (1 + R) × ExecutionEffort]

Where:
  R = Fraction of test re-runs (regression)
```

## Sanity Checks

> "A sanity check is a final check to see whether your answer makes sense in the context of the problem." {% cite kaner2000measurement %}

**Validation approaches:**
- Compare with function point estimates
- Check against industry ratios
- Use alternative estimation methods
- Testing is typically ~30% of total development effort

**Example validation:**
- FPA with Productivity 10 FP/MM
- Testing ≈ 30% of total effort

---

### References

{% bibliography --cited %}

---

{: .highlight }
**Disclaimer:** AI is used for text summarization, polishing and explaining. Authors have verified all facts and claims. In case of an error, feel free to file an issue.
