---
title: Defect Classification
parent: Cost of Quality
nav_order: 3
layout: default
---

# Defect Classification Schemes

Defect Classification Schemes provide a structured methodology for technical teams to categorize software anomalies, enabling objective feedback on development processes and identification of systemic quality gaps {% cite chillarege2000odc %} {% cite butcher2002improving %}.

## Orthogonal Defect Classification (ODC)

ODC is a methodology developed by IBM that uses a set of non-redundant (orthogonal) attributes to span the defect information space {% cite chillarege2000odc %}. It is specifically designed to provide objective, data-based decision support for technical teams, not just management {% cite butcher2002improving %}.

### Submittor Attributes (Classified at Detection)

| Attribute | Description | Examples |
|-----------|-------------|----------|
| **Activity** | Process step exposing the defect | Code Inspection, Function Test |
| **Trigger** | Condition required to expose defect | Coverage, Variation, Sequencing, Interaction |
| **Impact** | Actual or perceived customer impact | Usability, Reliability, Performance |

**Trigger Types:**
- Coverage, Variation, Sequencing
- Interaction, Workload/Stress
- Recovery/Exception
- Software Configuration

### Responder Attributes (Classified at Fix)

| Attribute | Description | Values |
|-----------|-------------|--------|
| **Target** | Entity that was fixed | Design, Code, Documentation |
| **Defect Type** | Nature of the correction | See below |
| **Qualifier** | Specificity of change | Missing, Incorrect, Extraneous |

**Defect Types:**
- Assignment/Initialization
- Checking
- Algorithm/Method
- Function/Class/Object
- Timing/Serialization
- Interface/OO Messages
- Relationship

### Process Feedback Through Signatures

ODC provides feedback through "signatures"—characteristic patterns of defect distributions {% cite butcher2002improving %}:

> *If a team finds 60% of defects in base code with only single-function triggers, the product is likely not ready for release, as complex interaction testing has not yet matured.*

## HP's Defect Origins, Types, and Modes

The HP model is designed to maximize process improvement during project retrospectives {% cite huber1999comparison %}:

### Critical Comparison to ODC

| Aspect | ODC | HP Model |
|--------|-----|----------|
| **Focus** | Where the fix was implemented | Where defect could have been prevented |
| **Terminology** | "Target" | "Origin" |
| **Finding** | 76% Code defects | 63% Design defects |

The fundamental semantic difference: ODC's "Target" identifies where the fix was implemented, while HP's "Origin" identifies the first activity where the defect could have been **prevented** {% cite huber1999comparison %}.

### Defect Cost Weighting

HP applies industry-derived multipliers showing that not all defects are equal {% cite huber1999comparison %}:

| Origin Phase | Cost Multiplier |
|--------------|-----------------|
| **Specification** | 14.25× |
| **Design** | 6.25× |
| **Code** | 2.5× |

This demonstrates the economic superiority of early-phase prevention.

## LiDeC (Lightweight Defect Classification)

LiDeC was developed for embedded automotive software where source code is often supplier-owned, limiting an OEM's ability to perform fine-grained analysis {% cite mellegard2012lightweight %}:

### Design Goals

- Minimize "process footprint" by raising abstraction level
- Reduce classification effort (vs. 19 minutes per defect for standard Root Cause Analysis)
- Support distributed development environments
- Enable safety-specific tracking (ISO 26262)

### Four Lifecycle Phases

| Phase | Purpose |
|-------|---------|
| **Recognition** | Discovery data (who, when, where found) |
| **Analysis** | Underlying cause, injection activity |
| **Resolution** | Impact, required verification |
| **Post-mortem** | Final state, lessons learned |

### Key Difference from ODC

LiDeC replaces fine-grained code categories with high-level characterizations and adds **safety-specific attributes** {% cite mellegard2012lightweight %}:

- Functional Safety Impact
- ASIL-classified requirements (per ISO 26262)
- Supplier vs. OEM responsibility tracking

## Origin/Where-Found Matrix

This matrix from Kan is a cross-classification tool that maps the origin phase of a defect against the detection phase {% cite kan2002metrics %}:

### Matrix Structure

|  | Design Review | Code Inspect | Unit Test | System Test | **Field** |
|--|---------------|--------------|-----------|-------------|-----------|
| **Requirements** | 5 | 2 | 1 | 3 | **8** |
| **Design** | 10 | 5 | 3 | 7 | **4** |
| **Code** | — | 15 | 20 | 10 | **2** |

### Identifying Testing Gaps

- **High diagonal** = Defects caught in same phase they were injected (proactive)
- **High "Field" column** = V&V activities failed; defects escaped to customers
- **Row totals > Column totals** = Early injections exceed early removals

**Application:** Justifies investments in earlier inspections if Row Totals (injections) exceed Column Totals (removals) in early stages {% cite kan2002metrics %}.

## Connection to Cost of Quality

Defect classification is the bridge between technical findings and the language of money used by upper management {% cite houston1999cost %}:

### Prevention vs. Failure Tracking

Classification allows organizations to track the shift from:
- **External Failure costs** (customer complaints, reputation damage)
- **To Prevention and Appraisal costs** (training, formal inspections)

### ROI Evidence

Raytheon data shows that systematic defect tracking supports dramatic improvement {% cite houston1999cost %}:

| Metric | CMM Level 1 | CMM Level 3 |
|--------|-------------|-------------|
| Total CoSQ | ~65% | ~20% |
| Rework costs | ~50% | <10% |

### The 1:10:100 Rule

Classification schemes prove that a defect caught in requirements ($1) is 100× cheaper than one found after release ($100+), justifying the "front-loading" of quality processes {% cite knox1993modeling %}.

## Choosing a Classification Scheme

| Scheme | Best For | Overhead |
|--------|----------|----------|
| **ODC** | Detailed technical process feedback | High |
| **HP Model** | Retrospective prevention focus | Medium |
| **LiDeC** | Embedded/automotive, safety-critical | Low |
| **Origin Matrix** | Quick gap analysis | Low |

---

### References

{% bibliography --cited %}

---

{: .highlight }
**Disclaimer:** AI is used for text summarization, polishing and explaining. Authors have verified all facts and claims. In case of an error, feel free to file an issue.
