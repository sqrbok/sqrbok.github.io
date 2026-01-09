---
title: Domain-Specific V&V
parent: Quality Planning
nav_order: 7
layout: default
---

# Domain-Specific V&V

Different application domains have unique V&V requirements driven by safety regulations, environmental constraints, and system complexity. This page covers V&V approaches for robotic systems, IoT, automotive, and model-based systems.

## Robotic and Autonomous Systems

A systematic review of 195 primary studies (from 10,709 initial results) reveals that V&V of RAS requires non-trivial extension of traditional testing techniques {% cite araujo2022ras %}:

### Key Challenges

| Challenge | Description |
|-----------|-------------|
| **Multi-disciplinary Complexity** | Integration of control, mechanical, electronic, and software engineering |
| **Environmental Unpredictability** | Dynamic environments with unknown boundary conditions |
| **Human-Machine Interaction** | Validating safety and social norms of robot-human interactions |
| **State-Space Explosion** | Massive design/input space that manual analysis cannot handle |

### V&V Approaches for RAS

| Approach | Description | Tools |
|----------|-------------|-------|
| **Formal Verification** | Most widely used; temporal logics, state-machines | Prism, Uppaal |
| **Simulation** | Virtual environments for scenario coverage | Gazebo, Matlab/Simulink, Unity-3D |
| **Runtime Monitoring** | Checking properties during execution | — |
| **Hardware-in-the-loop** | Testing with actual hardware components | — |
| **Metamorphic Testing** | Testing without explicit oracles | — |

### Research Gaps

- Only 10% of interventions evaluated in industrial setting
- Lack of rigorous metrics for efficiency/effectiveness/adequacy
- Under-explored: marine, submarine, space-based RAS

## IoT Systems Testing

A systematic review of 83 primary studies (2012-2022) identified 47 distinct quality attributes for IoT testing {% cite minani2024iot %}:

### Testing Objectives (Top Priorities)

| Objective | Frequency | Focus |
|-----------|-----------|-------|
| **Interoperability** | 20.4% | Communication between diverse devices |
| **Performance** | 20.4% | Latency, throughput, resource usage |
| **Scalability** | 15.6% | Performance under increasing load |
| **Usability** | 12.0% | User-centric validation |
| **IoT-Specific** | — | Connectivity, energy efficiency, device lifespan, dynamicity |

### Testing Approaches

| Technique | Description |
|-----------|-------------|
| **Fuzzy Testing** | Most researched; robustness against malformed inputs |
| **Protocol Testing** | Verify MQTT, CoAP communication |
| **Penetration Testing** | Identify security vulnerabilities |
| **Model-Based Testing** | Generate tests from models |
| **Log Analysis** | Post-execution fault detection |

### Tools & Testbeds

- **User tools:** Selenium, Apache JMeter, PatrIoT, Héctor, F-Interop
- **Testbeds:** FIT IoT-Lab (thousands of wireless devices), FogTestBed

### Key Challenges

| Challenge | Description |
|-----------|-------------|
| **Heterogeneity at Scale** | Hard to identify which devices cause faults |
| **Data/API Limitations** | Different formats, many devices lack APIs |
| **Cost of Realism** | Real-world testing expensive; simulations miss actual behavior |
| **Dynamic Unpredictability** | Non-repeatable scenarios complicate bug reproduction |

## Automotive Embedded Software

A systematic review of 62 primary studies (2011-2022) confirms the V-Model as the dominant SDLC for automotive testing {% cite arcanjo2023automotive %}:

> "The V&V process for embedded automotive software is complex, time-consuming, and expensive. However, it is an essential step to ensure the reliability of the overall vehicle system."

### ISO 26262 Alignment

| ASIL Level | Safety Impact | V&V Requirements |
|------------|---------------|------------------|
| **ASIL D** | Catastrophic risk | Highest safety requirements, formal methods |
| **ASIL C** | Severe injury | High coverage requirements |
| **ASIL B** | Possible injury | Structured testing |
| **ASIL A** | Minor injury | Basic testing |
| **QM** | No safety impact | Quality management only |

### In-the-Loop V&V Progression

| Technique | Description | Responsibility |
|-----------|-------------|----------------|
| **Model-in-the-loop (MIL)** | Evaluate software design with plant model | Supplier |
| **Software-in-the-loop (SIL)** | Simulation based on source code, digital plant | Supplier |
| **Hardware-in-the-loop (HIL)** | Software in physical ECU, real-time infrastructure | Supplier/OEM |
| **Vehicle-in-the-loop (VIL)** | Controlled environment with realistic sensor inputs | OEM |

### Testing Types

- **Functional tests** — Black-box testing of requirements
- **Application tests** — Vehicle variants in real road conditions
- **Homologation tests** — Regional compliance (laws vary by country)

### Gap: Autonomous Vehicles

ISO 26262 is not ideal for autonomous vehicles—it does not adequately cover unpredictable nature and dynamic boundary conditions.

## Model-Based Systems Engineering

MBSE requires V&V of models before implementation {% cite cederbladh2023vv %}:

### Models as Primary Artifacts

In MBSE, models are not just documentation—they are the primary engineering artifacts:

- **SysML models** — System architecture and requirements
- **Simulink models** — Control algorithms and behavior
- **State machines** — System states and transitions

### Early V&V Techniques

| Technique | Description | Adoption |
|-----------|-------------|----------|
| **Model transformations** | Automated conversion between languages | 63% |
| **Simulation** | Execute models to verify behavior | Common |
| **Model checking** | Formal verification of properties | Growing |
| **Reviews** | Engineering review of model artifacts | Standard |

### Quality Gates for Models

| Gate | Criteria |
|------|----------|
| **Model completeness** | All requirements traced |
| **Deadlock-freeness** | No blocking states |
| **Consistency** | No contradictions between views |
| **Transformability** | Model can be transformed to implementation |

## Cross-Domain Patterns

Patterns common across safety-critical domains:

### Criticality-Driven V&V Intensity

| Criticality | V&V Intensity |
|-------------|---------------|
| High | Full coverage, formal methods, independent V&V |
| Medium | Structural testing, reviews |
| Low | Functional testing |

### Common Requirements

1. **Traceability** — Requirements → Design → Code → Tests
2. **Independence** — V&V separate from development
3. **Documentation** — Comprehensive evidence for certification
4. **Regression** — Ensure changes don't break existing functionality

### Tool Ecosystem

| Domain | Common Tools |
|--------|--------------|
| Automotive | DOORS, Polarion, VectorCAST |
| Aerospace | LDRA, Polyspace, Simulink |
| IoT | MQTT testing tools, security scanners |
| Robotics | ROS testing, Gazebo simulation |

---

### References

{% bibliography --cited %}

---

{: .highlight }
**Disclaimer:** AI is used for text summarization, polishing and explaining. Authors have verified all facts and claims. In case of an error, feel free to file an issue.
