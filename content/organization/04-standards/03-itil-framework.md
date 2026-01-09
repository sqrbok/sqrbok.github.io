---
title: ITIL Framework
parent: Quality Standards
nav_order: 3
layout: default
---

# ITIL Framework

The Information Technology Infrastructure Library (ITIL) is the global de facto standard for IT Service Management (ITSM), providing a framework of best practices to align IT services with business needs {% cite itil2007v3 %} {% cite iden2013itil %}. While ITSM is the general concept of managing the IT function as a service provider, ITIL is the specific set of prescribed practices used to achieve it.

## ITIL Overview and Service Lifecycle

ITIL v3 (introduced in 2007) shifted the focus from process-oriented management to a Service Lifecycle approach, emphasizing how an IT service moves from conception to delivery and improvement {% cite itil2007v3 %}.

### The Five Phases of the Service Lifecycle

| Phase | Focus | Key Activities |
|-------|-------|----------------|
| **Service Strategy** | Business value and competitive advantage | Capacity development, resource planning |
| **Service Design** | Designing services for live environment | Service catalogs, SLAs, capacity management |
| **Service Transition** | Validation and deployment | Testing, change implementation |
| **Service Operation** | Daily service delivery | Incident resolution, operational management |
| **Continual Service Improvement** | Ongoing enhancement | 7-step improvement process |

### Phase Details

**Service Strategy**: The core of the lifecycle; it focuses on developing capacities and planning resources to provide a competitive advantage and business value {% cite itil2007v3 %}.

**Service Design**: Responsible for designing new or changed services for the live environment, including service catalogs, service level agreements (SLAs), and capacity/availability management.

**Service Transition**: Manages the validation, testing, and deployment of services into production, ensuring that changes are implemented effectively.

**Service Operation**: The most critical phase for customer perception; it focuses on daily management practices to deliver services at agreed-upon levels and solve operational problems.

**Continual Service Improvement (CSI)**: Uses a "7-step improvement process" to monitor and assess the quality of services, ensuring they continue to meet evolving business requirements.

## Core ITIL Processes

Among the many processes defined within the lifecycle, three are considered foundational for maintaining stability and quality {% cite iden2013itil %}:

### Incident Management (Service Operation)

**Purpose**: Restore normal service operation as quickly as possible following a disruption to minimize impact on the business.

Key activities:
- Incident detection and recording
- Classification and prioritization
- Investigation and diagnosis
- Resolution and recovery
- Closure and documentation

### Problem Management (Service Operation)

**Purpose**: Identify the root causes of incidents to prevent them from recurring, shifting the IT team from "firefighting" to proactive resolution.

Key activities:
- Problem detection and logging
- Root cause analysis
- Workaround development
- Known error documentation
- Permanent resolution

### Change Management (Service Transition)

**Purpose**: Standardize methods for efficient and prompt handling of all changes to IT infrastructure to minimize the risk of service downtime.

Key activities:
- Change request submission
- Impact and risk assessment
- Change approval (CAB)
- Implementation planning
- Post-implementation review

## ITIL Evolution

ITIL has evolved significantly since its inception by the UK's Central Computer and Telecommunications Agency (CCTA) {% cite iden2013itil %}:

| Version | Year | Description |
|---------|------|-------------|
| **ITIL V1** | 1980s | 31 associated books covering IT service provision |
| **ITIL V2** | 2000-2002 | Consolidated into 7 connected books; became universal standard |
| **ITIL v3** | 2007 | 5 core volumes representing lifecycle phases |
| **ITIL 2011** | 2011 | Revised v3 for consistency improvements |
| **ITIL 4** | 2019 | Focus on value co-creation and modern practices |

### V2 to V3 Transition

The transition from V2 to v3 represented a fundamental shift {% cite itil2007v3 %}:
- From **process-focused** to **service lifecycle-focused**
- From **operational efficiency** to **business value alignment**
- From **IT-centric** to **customer-centric** perspective

## Benefits and Organizational Value

Research indicates that ITIL adoption is primarily motivated by the desire to improve operational efficiency, service orientation, and customer satisfaction {% cite iden2013itil %}:

### Adoption Statistics

| Metric | Finding |
|--------|---------|
| US IT managers using ITIL | **45%** (2009 survey) |
| Planning to adopt | **15%** additional |
| Firms at CMM Level 2 | **31%** of itSMF members |
| Firms at CMM Level 3 | **25%** of itSMF members |

### Reported Performance Improvements

Organizations implementing ITIL report {% cite iden2013itil %}:
- **Improved response times**: Faster incident resolution
- **Reduced downtime**: Better service availability
- **Better resource utilization**: Optimized IT capacity
- **Standardized processes**: Consistent service delivery
- **Higher ROI**: Long-term financial gains through maturity

### Primary Adoption Motivations

| Motivation | Priority |
|------------|----------|
| Operational efficiency | High |
| Service orientation | High |
| Customer satisfaction | High |
| Cost reduction | Lower initial, improves with maturity |

---

### References

{% bibliography --cited %}

---

{: .highlight }
**Disclaimer:** AI is used for text summarization, polishing and explaining. Authors have verified all facts and claims. In case of an error, feel free to file an issue.
