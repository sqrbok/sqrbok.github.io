---
title: TMMi & Maturity Models
parent: Quality Standards
nav_order: 6
layout: default
---

# TMMi & Other Maturity Models

Maturity models serve as structured frameworks that allow organizations to analyze behaviors, practices, and processes to achieve reliable and sustainable results {% cite mikusova2020maturity %}. While the Capability Maturity Model Integration (CMMI) is a global standard for overall software development, the Test Maturity Model Integration (TMMi) emerged to provide specific, dedicated guidance for software testing practices {% cite vanveenendaal2022tmmi %}.

## TMMi Overview and Structure

The TMMi was developed to address a gap in general process improvement models like CMMI and SPICE, which often lack detailed recommendations for software testing despite it accounting for a significant portion of project budgets {% cite vanveenendaal2022tmmi %}.

### Foundation

- **Formally established**: 2010 by the TMMi Foundation
- **First stable specification (v1.0)**: Published 2012
- **Alignment**: Heavily aligned with ISTQB standards and terminology

### Hierarchical Structure

TMMi is designed as a staged meta-model {% cite vanveenendaal2022tmmi %}:

| Component | Count |
|-----------|-------|
| Maturity Levels | 5 |
| Process Areas (PAs) | 16 |
| Specific Goals (SG) | 50 |
| Specific Practices (SP) | 173 |
| Generic Goals (GG) | Institutionalization objectives |
| Generic Practices (GP) | Implementation activities |

## TMMi Levels and Characteristics

TMMi provides a roadmap for evolving testing from an ad-hoc activity to an optimized process {% cite vanveenendaal2022tmmi %}:

### Level Overview

| Level | Name | Focus |
|-------|------|-------|
| **1** | Initial | Unmanaged, ad-hoc, chaotic |
| **2** | Managed | Basic test management |
| **3** | Defined | SDLC integration |
| **4** | Measured | Quantitative evaluation |
| **5** | Optimization | Continuous improvement |

### Level Details

**Level 1 - Initial**: Testing is unmanaged, ad-hoc, and often chaotic. Success depends on individual effort.

**Level 2 - Managed**: Focuses on basic management with key process areas:
- Test Policy and Strategy
- Test Planning
- Test Monitoring and Control
- Test Design and Execution
- Test Environment

**Level 3 - Defined**: Integration of testing into the SDLC with key process areas:
- Non-Functional Testing
- Peer Reviews
- Test Training Programs
- Test Organization
- Test Lifecycle Integration

**Level 4 - Measured**: Testing is measured and evaluated:
- Test Measurement
- Product Quality Evaluation
- Advanced Peer Reviews

**Level 5 - Optimization**: Focuses on continuous improvement:
- Defect Prevention
- Test Process Optimization
- Quality Control

## Adoption Motivations and Benefits

According to a 2020 international survey of 74 certified companies, TMMi adoption is driven by the "Golden Triangle" of project management {% cite vanveenendaal2022tmmi %}:

### Top Motivations

| Motivation | Percentage |
|------------|------------|
| Enhancing software quality | **70%** |
| Increasing testing productivity | **68%** |
| Reducing product risk | **62%** |
| Achieving formal certification | **62%** |

### Reported Benefits

| Benefit Area | Improvement Rate |
|--------------|------------------|
| Product Quality | **88%** observed improvement |
| Compliance | **84%** improved standardization |
| Test Efficiency | **77%** noted productivity gains |
| Satisfaction | **87%** met or exceeded expectations |

### Specific Improvements Reported

| Metric | Before | After |
|--------|--------|-------|
| Defect leakage to production | 10% | 5% |
| Regression test cycle | 4 hours | 30 minutes |

## Comparison of Maturity Models

The landscape of maturity models is vast, with at least 58 distinct models reported for testing alone {% cite vanveenendaal2022tmmi %}.

### CMMI vs TMMi

| Aspect | CMMI | TMMi |
|--------|------|------|
| **Scope** | Overall SDLC | Testing-specific |
| **Testing guidance** | Limited | Comprehensive |
| **Use case** | Defense/government projects | Testing process improvement |
| **Relationship** | Primary framework | Specialized complement |

CMMI is an "overall" SDLC model often required for defense or government projects, but it does not provide specific testing guidelines. TMMi acts as a specialized complement that fills this testing-specific gap {% cite vanveenendaal2022tmmi %}.

### Other Maturity Model Categories

| Category | Examples | Focus |
|----------|----------|-------|
| **General Process** | CMMI, SPICE/ISO 15504 | Overall software development |
| **Testing-Specific** | TMMi, TPI | Software testing practices |
| **Usability** | UCDM, UMM-P | User-centered design |
| **Academic** | eMM, ICMM | Education, knowledge management |

### Maturity Model Landscape

Research by Mikušová & Čambál (2020) examines the application of maturity models across various domains {% cite mikusova2020maturity %}:

- **Usability Maturity Models (UCMMs)**: Most are directly based on consolidated standards like CMMI or ISO/IEC 15504
- **Academic Maturity Models**: Adapted for specific purposes such as e-Learning (eMM) and Intellectual Capital (ICMM)
- **Evolving Trends**: Modern models shifting toward agility and automation

### Selecting a Maturity Model

| Consideration | Questions to Ask |
|---------------|------------------|
| **Scope** | Overall process or specific domain? |
| **Compliance** | Certification requirements? |
| **Resources** | Available budget and expertise? |
| **Integration** | Existing frameworks in use? |

## Summary: When to Use Which Model

| Need | Recommended Model |
|------|-------------------|
| Overall software development maturity | CMMI |
| Testing-specific improvement | TMMi |
| IT service management | ITIL |
| Quality management system | ISO 9001 |
| Combined development + testing | CMMI + TMMi together |

---

### References

{% bibliography --cited %}

---

{: .highlight }
**Disclaimer:** AI is used for text summarization, polishing and explaining. Authors have verified all facts and claims. In case of an error, feel free to file an issue.
