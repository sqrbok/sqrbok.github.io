---
title: PSP & TSP
parent: Industry Practices
nav_order: 5
layout: default
---

# Personal Software Process & Team Software Process

The Personal Software Process (PSP) and Team Software Process (TSP) are disciplined methodologies designed to improve software quality and project predictability by transferring process management skills directly to individual engineers and their teams {% cite humphrey1995discipline %} {% cite hayes1997psp %} {% cite mcandrews2000tsp %}.

## Personal Software Process (PSP) Methodology

The PSP is a defined and measured process designed for individual use to guide the planning and development of software modules {% cite humphrey1995discipline %}. It is structured into seven process levels (PSP0 to PSP2.1) that use a "self-convincing" learning strategy, where engineers use their own data to see the impact of disciplined methods on their performance.

### Methodology Focus

Engineers follow defined scripts to plan, design, code, and review software, recording:
- **Time**: Effort spent on each activity
- **Defects**: Type, injection phase, removal phase
- **Product Size**: Lines of code, function points

### Key Techniques

| Technique | Purpose |
|-----------|---------|
| **PROBE Method** | Proxy-Based Estimating for size and effort forecasting |
| **Checklist-guided Reviews** | Personal design and code reviews to improve quality |
| **Earned Value** | Schedule tracking and progress measurement |

## Hayes & Over (1997) Study Results

This foundational study analyzed the performance of 298 software engineers across 23 classes {% cite hayes1997psp %}:

### Estimation Accuracy

| Metric | Improvement Factor |
|--------|-------------------|
| Size estimation accuracy | **2.5x** improvement |
| Effort estimation accuracy | **1.75x** improvement |

### Quality Gains

- **Product quality** (defects found in unit tests): **2.5x** improvement
- **Process yield** (defects removed before first compile): increased by **50%**

### Key Finding: Quality Without Productivity Loss

The study found **no significant change in personal productivity** (LOC/hour), meaning quality gains were achieved without a loss in efficiency {% cite hayes1997psp %}.

### Bias Correction

The initial bias toward underestimating both size and effort shifted to a more balanced mix of over- and underestimates, allowing errors to cancel each other out in larger projects.

## Team Software Process (TSP) Overview

The TSP provides a team environment that supports disciplined PSP work and builds self-directed teams capable of managing their own projects {% cite mcandrews2000tsp %}.

### The TSP Launch

A critical four-day, nine-meeting process where the entire team (and management) {% cite mcandrews2000tsp %}:
- Sets goals and objectives
- Assigns roles (Quality Manager, Planning Manager, etc.)
- Creates a detailed, balanced plan
- Establishes team working agreements

### Team Roles

| Role | Responsibility |
|------|----------------|
| **Team Leader** | Overall coordination and external interface |
| **Planning Manager** | Schedule and resource planning |
| **Quality Manager** | Process quality and defect tracking |
| **Process Manager** | Process adherence and improvement |
| **Support Manager** | Tools and infrastructure |

### Organizational Adoption

Adoption typically starts with pilot projects. Successful implementation requires {% cite mcandrews2000tsp %}:
- Executive training (1.5 days)
- Middle-management training (3 days)
- PSP training for all participating engineers (2 weeks)

## Quality and Productivity Results from TSP in Practice

Summary data from 20 TSP projects across 13 organizations (including Microsoft, Xerox, and Boeing) demonstrate performance that exceeds typical industry standards {% cite davis2003tsp %}:

### Schedule Performance

TSP teams delivered products an average of only **6% later than planned**, with a range of 20% early to 27% late {% cite davis2003tsp %}.

### Productivity Improvements

| Organization | Productivity Improvement |
|--------------|-------------------------|
| Average across organizations | **78%** improvement |
| Hill Air Force Base (first project) | **123%** improvement |

### Delivered Quality

TSP software quality is often **two orders of magnitude higher** than typical products {% cite davis2003tsp %}:

| Metric | TSP Projects | Industry Typical |
|--------|-------------|------------------|
| Defects/KLOC | **0.06** | 7.5 |

## Key Metrics and Defect Reduction Findings

TSP shifts the focus from defect detection (testing) to defect prevention through rigorous reviews and inspections {% cite davis2003tsp %}.

### Yield as Primary Metric

**Yield** is the primary process quality metric—the percentage of defects removed before system test {% cite hayes1997psp %}:
- Mature TSP teams achieve an average of **0.4 defects/KLOC** in system test
- Several teams report **zero defects** in system test

### Reduction in Rework

Compared to previous releases, TSP teams achieved {% cite davis2003tsp %}:
- **10x reduction** in problems logged by testing groups
- **8x reduction** in system test duration

### Cost of Quality (COQ)

| Activity | TSP Projects | Industry Norm |
|----------|-------------|---------------|
| System testing effort | **4%** of total | 40% of total |
| Failure COQ reduction | **58%** average | — |

## Summary: PSP/TSP Benefits

| Dimension | PSP Benefits | TSP Benefits |
|-----------|-------------|--------------|
| **Quality** | 2.5x defect reduction | 0.06 defects/KLOC |
| **Estimation** | 2.5x size accuracy | 6% schedule variance |
| **Productivity** | No loss with quality gains | 78% average improvement |
| **Learning** | Self-convincing with own data | Team synergy and roles |

---

### References

{% bibliography --cited %}

---

{: .highlight }
**Disclaimer:** AI is used for text summarization, polishing and explaining. Authors have verified all facts and claims. In case of an error, feel free to file an issue.
