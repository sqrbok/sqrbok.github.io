---
title: Defect Injection & Removal
parent: Cost of Quality
nav_order: 2
layout: default
---

# Defect Injection and Removal Models

Defect Injection and Removal Models provide a mathematical and conceptual framework for understanding how errors enter a software system and how various quality activities filter them out before the product reaches the customer {% cite chulani1999coqualmo %} {% cite jones2008applied %}.

## The "Tank and Pipes" Model

Originally proposed by Capers Jones in 1975, this is the simplest model for understanding defect flow through the development process {% cite jones2008applied %}:

### How It Works

| Component | Role | Description |
|-----------|------|-------------|
| **Introduction pipes** | Defect entry | Defects flow in during Requirements, Design, and Code phases |
| **The tank** | Defect backlog | Cumulative pool of defects residing in the software |
| **Removal pipes** | V&V filters | Reviews, unit testing, system testing drain defects |
| **Residual defects** | Customer impact | What remains becomes external failure costs |

The model makes it intuitive that we can reduce residual defects either by reducing what flows in (prevention) or by improving what we remove (appraisal effectiveness) {% cite wyrwa2008software %}.

## COQUALMO (Constructive Quality Model)

Developed at USC by Chulani and Boehm, COQUALMO extends the COCOMO II cost model to relate defectivity to project cost and schedule {% cite chulani1999coqualmo %}:

### Defect Introduction Submodel

Predicts defects introduced (DI) based on size and 21 Quality Adjustment Factors:

| Phase | Nominal Rate (defects/KSLOC) |
|-------|------------------------------|
| Requirements | **10** |
| Design | **20** |
| Code | **30** |

Rates are adjusted by drivers such as Analyst Capability (ACAP), Product Complexity (CPLX), Process Maturity (PMAT), and Tool Support (TOOL) {% cite chulani1999coqualmo %}.

### Defect Removal Submodel

Three primary removal activities with Defect Removal Fraction (DRF) ratings from "Very Low" to "Extra High" {% cite chulani1999coqualmo %}:

| Activity | Focus | DRF Range |
|----------|-------|-----------|
| **Peer Reviews** | Static analysis of artifacts | VL to XH |
| **Automated Analysis** | Tools, linters, static analyzers | VL to XH |
| **Execution Testing** | Dynamic testing activities | VL to XH |

## Process Signatures

A process signature is a graphical profile showing cumulative defects injected versus removed across the lifecycle {% cite kan2002metrics %}:

### Baseline Example

| Phase | Cumulative Injected | Removed (50% each test) | Residual |
|-------|---------------------|-------------------------|----------|
| Requirements | 10 | 0 | 10 |
| High-Level Design | 20 | 0 | 20 |
| Low-Level Design | 40 | 0 | 40 |
| Coding | **80** | 0 | 80 |
| Unit Testing | 80 | 40 | 40 |
| Integration Testing | 80 | 60 | 20 |
| System Testing | 80 | 70 | **10** |

**Key insight:** The vertical gap between "Injected" and "Removed" curves at shipment represents latent faults that escape to customers {% cite kan2002metrics %}.

## Improvement Scenarios

Organizations use these models to evaluate two primary strategies for reducing residual defects:

### Scenario 1: Better Testing

Increase the yield of existing test phases:

| Configuration | UT | IT | ST | Residual |
|--------------|-----|-----|-----|----------|
| Baseline | 50% | 50% | 50% | 10 |
| **Improved UT** | **70%** | 50% | 50% | **6** |

### Scenario 2: Introducing Inspections

Add prevention/appraisal steps earlier in the cycle:

| Phase | Injected | Inspection (20%) | After Inspection |
|-------|----------|------------------|------------------|
| Requirements | 10 | 2 removed | 8 |
| HLD | 16 | 3 removed | 13 |
| LLD | 26 | — | 26 |
| Coding | 52 | 10 removed | 42 |

After testing (50% each): **6 residual defects**

### Comparison

| Scenario | Final Residual | Economic Impact |
|----------|----------------|-----------------|
| Better Testing | 6 | Higher cost per defect (later detection) |
| **Inspections** | 6 | **Lower cost** (earlier detection) |

Both reach the same quality goal, but inspections are often economically superior because they catch defects in design phases where fixes are significantly cheaper {% cite houston1999cost %}.

## Connection to Cost of Quality

Defect models translate technical performance into financial outcomes to justify process investments {% cite houston1999cost %} {% cite knox1993modeling %}:

### The 1:10:100 Rule

| Phase Found | Relative Cost |
|-------------|---------------|
| Requirements | **$1** |
| Development | **$10** |
| Post-release | **$100+** |

Models prove that "shifting left" avoids this exponential cost growth.

### Defect Weighting

Not all defects are equal. Research suggests fixing a Specification defect is **14.25× more expensive** than a Code defect due to the "rework cascade" required to update documentation and design {% cite kan2002metrics %}.

### Empirical Evidence: Raytheon

Real-world data shows significant ROI from prevention investment {% cite houston1999cost %}:

| Metric | CMM Level 1 | CMM Level 3 |
|--------|-------------|-------------|
| Total CoSQ (% of project) | ~65% | ~20% |
| Rework (failure costs) | ~50% | <10% |

This represents a **3× reduction** in total CoSQ and **5× reduction** in rework costs.

## Practical Analogy

Defect injection and removal is like a water filtration system:

- **Defect injection** = sediment entering pipes at different points
- **Reviews and testing** = filters at various stages
- **Scenario 1 (Better Testing)** = buying a bigger, more expensive filter at the tap
- **Scenario 2 (Inspections)** = placing small, inexpensive screens at every joint

The Cost of Quality tells you it is much cheaper to clean a small screen weekly than to replace an entire water heater clogged with accumulated sediment.

---

### References

{% bibliography --cited %}

---

{: .highlight }
**Disclaimer:** AI is used for text summarization, polishing and explaining. Authors have verified all facts and claims. In case of an error, feel free to file an issue.
