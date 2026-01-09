---
title: CMMI Overview
parent: Quality Standards
nav_order: 1
layout: default
---

# CMMI Overview

Capability Maturity Model Integration (CMMI) is an internationally recognized process improvement framework designed to provide software development organizations with the structure and stability necessary to enhance software quality, increase productivity, and minimize the risk of failure {% cite kuhrmann2016spi %}. Originally developed by the Software Engineering Institute (SEI) and now managed by ISACA, it serves as a roadmap for organizations to evolve their processes from ad hoc activities to disciplined, optimized systems.

## CMMI Structure

The CMMI structure is a hierarchical meta-model that organizes best practices into manageable components {% cite cmmi-dev-2010 %}:

| Component | Description |
|-----------|-------------|
| **Process Areas (PAs)** | Groups of related practices that satisfy improvement goals |
| **Specific Goals (SG)** | Unique objectives for a single process area |
| **Specific Practices (SP)** | Concrete activities to achieve specific goals |
| **Generic Goals (GG)** | Objectives that apply to every process area |

### Generic Goals Components

Generic goals ensure processes are institutionalized and sustained {% cite cmmi-dev-2010 %}:
- **Commitment to Perform**: Policies and sponsorship
- **Ability to Perform**: Resources and training
- **Directing Implementation**: Measurement and analysis
- **Verification**: Conformance audits

## Maturity and Capability Levels

CMMI offers two distinct representations for evaluation {% cite cmmi-dev-2010 %}:

| Representation | Focus |
|----------------|-------|
| **Staged** | Organization's overall maturity |
| **Continuous** | Individual process areas |

### Maturity Levels (Staged Representation)

Organizations progress through five levels, where each level serves as the necessary foundation for the next {% cite cmmi-dev-2010 %}:

| Level | Name | Characteristics |
|-------|------|-----------------|
| **1** | Initial | Ad hoc, chaotic; success depends on individual heroics |
| **2** | Managed | Processes planned, performed, and controlled at project level |
| **3** | Defined | Processes standardized at organization level |
| **4** | Quantitatively Managed | Quantitative objectives; statistical analysis for decisions |
| **5** | Optimizing | Continuous improvement through innovation |

#### Level Details

**Level 1 - Initial**: Processes are usually ad hoc and chaotic. Success depends on individual heroics rather than stable processes, often resulting in budget and schedule overruns.

**Level 2 - Managed**: Processes are planned, performed, and controlled at the project level. Discipline ensures that practices are retained even during times of stress.

**Level 3 - Defined**: Processes are well-characterized, understood, and standardized at the organization level. Consistency is achieved by tailoring the organization's set of standard processes to individual projects.

**Level 4 - Quantitatively Managed**: The organization establishes quantitative objectives for quality and performance. Detailed measures are collected and statistically analyzed to support fact-based decision-making.

**Level 5 - Optimizing**: The organization focuses on continuous improvement through incremental and innovative technological advancements based on a quantitative understanding of process variation.

### Capability Levels (Continuous Representation)

Capability levels characterize the maturity of an individual process area rather than the whole organization {% cite cmmi-dev-2010 %}:

| Level | Name | Description |
|-------|------|-------------|
| 0 | Incomplete | Process not performed or partially performed |
| 1 | Performed | Process satisfies specific goals |
| 2 | Managed | Process is planned and controlled |
| 3 | Defined | Process uses organizational standards |

## Process Areas and Categories

CMMI-DEV v1.3 organizes its 22 process areas primarily into four categories {% cite cmmi-dev-2010 %}:

| Category | Focus | Examples |
|----------|-------|----------|
| **Process Management** | Organizational processes | OPD, OPF, OPP |
| **Project Management** | Project planning and control | PP, PMC, IPM, RSKM |
| **Engineering** | Product development | REQM, RD, TS, PI, VER, VAL |
| **Support** | Supporting activities | CM, PPQA, MA, DAR, CAR |

### Level 2 Process Areas (Managed)

Focus on project basics:
- **Project Planning (PP)**: Establishing and maintaining plans
- **Requirements Management (REQM)**: Managing requirements
- **Configuration Management (CM)**: Establishing and maintaining integrity
- **Measurement and Analysis (MA)**: Data collection and analysis

### Level 3 Process Areas (Defined)

Focus on organizational consistency and advanced engineering:
- **Requirements Development (RD)**: Defining requirements
- **Technical Solution (TS)**: Design and implementation
- **Organizational Training (OT)**: Developing skills
- **Risk Management (RSKM)**: Identifying and mitigating risks
- **Decision Analysis and Resolution (DAR)**: Formal evaluation alternatives

## CMMI-DEV v1.3 to v2.0 Evolution

The transition to CMMI v2.0 (introduced in 2018) aimed to shift the focus from "checkbox compliance" to measurable performance and business alignment {% cite kuhrmann2016spi %}:

### Key Changes

| Aspect | v1.3 | v2.0 |
|--------|------|------|
| **Structure** | Three constellations (DEV, ACQ, SVC) | Single integrated model |
| **Terminology** | "Process Areas" | "Practice Areas" |
| **Agile Compatibility** | Challenges with integration | Designed for Agile, SAFe, DevSecOps |

### Performance Improvements

Empirical evidence from the CMMI Institute indicates v2.0 adoption leads to:
- **17% increase** in estimation accuracy
- **70% reduction** in rework
- **97% on-time** delivery rate

### Research Findings

CMMI is the most frequently studied standard in the software process improvement (SPI) field, although it is often criticized for its complexity and high implementation effort, leading to the development of more specialized frameworks for smaller companies {% cite kuhrmann2016spi %}.

---

### References

{% bibliography --cited %}

---

{: .highlight }
**Disclaimer:** AI is used for text summarization, polishing and explaining. Authors have verified all facts and claims. In case of an error, feel free to file an issue.
