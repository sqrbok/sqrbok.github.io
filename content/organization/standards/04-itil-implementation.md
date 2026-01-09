---
title: ITIL Implementation
parent: Quality Standards
nav_order: 4
layout: default
---

# ITIL Implementation

The implementation of the Information Technology Infrastructure Library (ITIL) framework is a complex organizational endeavor that requires moving from technology-centric attitudes to a customer-oriented service perspective {% cite iden2013itil %}.

## Implementation Approaches and Sequences

There is no single standardized or generally accepted procedure for implementing ITIL; however, researchers have identified common logical routes {% cite schmidtbauer2013itil %}.

### Standard 11-Step Sequence

Schmidtbauer et al. (2013) identify an exemplary implementation approach {% cite schmidtbauer2013itil %}:

| Step | Activity |
|------|----------|
| 1 | Project preparation |
| 2 | Service structure definition |
| 3 | Role selection |
| 4 | "As-is" analysis |
| 5 | "To-be" definition |
| 6 | Process interface definition |
| 7 | Establishing process control |
| 8 | Detailed process elaboration |
| 9 | Selection of application systems |
| 10 | Intensive training |
| 11 | Implementation |

### "Light" Sequence for SMEs

Cruz-Hinojosa & Gutiérrez-de-Mesa (2016) describe a sequence tailored for smaller firms {% cite cruzhinojosa2016itil %}:

1. Assess needs
2. Train at Foundation level
3. Create a tactical plan
4. Create a Configuration Management Database (CMDB)
5. Control Incident Management
6. Implement Problem and Change Management
7. Address specific business requirements

### Initial Focus

Most organizations begin their journey by adopting the **Incident Management** process to restore normal operations as quickly as possible following disruptions {% cite ahmad2013itil %}.

## ITIL in SMEs: Challenges and Adaptations

Small and Medium Enterprises (SMEs) face distinct challenges because the standard ITIL framework is often considered too large and resource-intensive for their limited labor and budgets {% cite cruzhinojosa2016itil %} {% cite schmidtbauer2013itil %}.

### Primary Barriers

| Barrier | Description |
|---------|-------------|
| **Technical talent** | Shortage of skilled personnel |
| **Financial resources** | Limited implementation budgets |
| **Framework complexity** | ITIL perceived as too comprehensive |
| **Documentation overhead** | Extensive documentation requirements |

### SME Adaptations

To keep operations "short and simple," SMEs often implement adaptations {% cite cruzhinojosa2016itil %} {% cite schmidtbauer2013itil %}:

| Adaptation | Approach |
|------------|----------|
| **"Light" ITIL** | Scaled-down ITSM landscape |
| **Hybrid processes** | Merge incident, request, and problem management |
| **Phased rollout** | Implement core processes first |
| **Simplified documentation** | Reduce administrative overhead |

### SME Advantages

Despite resource constraints, SMEs may have advantages {% cite cruzhinojosa2016itil %}:
- **Lower resistance to change** than large corporations
- **Faster culture transformation** possible
- **More rapid customer service focus** development

## Critical Success Factors (CSFs)

Successful ITIL adoption is largely dependent on human factors and user acceptance rather than just technical tool selection {% cite ahmad2013itil %}.

### Seven Key CSF Classes

Ahmad & Shamsudin (2013) identify 17 CSFs grouped into seven classes {% cite ahmad2013itil %}:

| Class | Examples |
|-------|----------|
| **Top management support** | Executive sponsorship, resource allocation |
| **Change management & culture** | Organizational readiness, cultural alignment |
| **Monitoring & evaluation** | KPIs, progress tracking |
| **Communication & cooperation** | Stakeholder engagement, collaboration |
| **Project management & governance** | Formal methodology, oversight |
| **Training & competence** | Staff education, certification |
| **Process implementation & technology** | Tool selection, process design |

### Stakeholder Priority Divergence

Findings show that priorities differ by role {% cite ahmad2013itil %}:

| Stakeholder Group | Top Priority |
|-------------------|--------------|
| IT Staff | Top management support |
| IT Management | Top management support |
| End-Users | Communication and cooperation |

### The Project Champion

Effective implementation often requires a **champion** to advocate for the framework and promote its benefits to stakeholders {% cite ahmad2013itil %}.

## Case Studies

### Nordex (Medium-Sized Enterprise)

The wind turbine manufacturer Nordex implemented ITIL Service Operation processes for its "product-related IT" {% cite schmidtbauer2013itil %}.

**Method**: Customized process flow diagrams according to specific requirements captured in workshops and modeling sessions.

**The 3-Layered Approach**:

| Layer | Focus |
|-------|-------|
| 1 | Organizational function of the Help Desk |
| 2 | Detailed ITIL V3 processes |
| 3 | Specific instructions/checklists for roles |

**Outcome**: Achieved **ISO 20000 certification in less than one year**.

### Financial Services (Failed Implementation → Recovery)

Ahmad & Shamsudin (2013) analyzed a financial firm in the UAE where the ITIL project initially failed {% cite ahmad2013itil %}.

**Initial Failure**:
- Took **five years** to implement only a few selected processes
- Lack of formal project management strategies
- Non-mandatory training
- Failure to communicate the "need for ITIL" to employees

**Resolution**:
- Applied Analytical Hierarchy Process (AHP) to re-evaluate stakeholder priorities
- Involved end-users in decision-making (previously excluded due to lack of technical background)
- Implemented structured communication plan

### Lessons Learned

| Success Factor | Nordex | Financial Services (Initial) |
|----------------|--------|------------------------------|
| Project management | Strong methodology | Weak/informal |
| Training | Intensive, mandatory | Non-mandatory |
| Communication | Stakeholder workshops | Poor communication |
| User involvement | Active engagement | End-users excluded |
| Timeline | < 1 year to ISO 20000 | 5 years, incomplete |

---

### References

{% bibliography --cited %}

---

{: .highlight }
**Disclaimer:** AI is used for text summarization, polishing and explaining. Authors have verified all facts and claims. In case of an error, feel free to file an issue.
