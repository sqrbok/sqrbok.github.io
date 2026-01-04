---
title: Microsoft Quality Practices
parent: Industry Practices
nav_order: 2
layout: default
---

# Microsoft Quality Practices

> **Reading time:** 5 min | **Level:** Intermediate

Microsoft has evolved its quality practices significantly over decades, from the "Windows quality crisis" to modern cloud-native development. This note covers key practices that emerged from this transformation.

---

## Security Development Lifecycle (SDL)

### Background

After major security incidents (Code Red, Nimda, SQL Slammer), Microsoft created SDL in 2004. Bill Gates' "Trustworthy Computing" memo made security a company priority.

### SDL Phases

| Phase | Activities |
|-------|------------|
| **Training** | Security training for all engineers |
| **Requirements** | Define security requirements, quality gates |
| **Design** | Threat modeling, attack surface analysis |
| **Implementation** | Secure coding standards, banned functions |
| **Verification** | Static analysis, dynamic analysis, fuzz testing |
| **Release** | Final security review, incident response plan |
| **Response** | Security response process for vulnerabilities |

### Key SDL Practices

**Threat Modeling:**
- STRIDE methodology (Spoofing, Tampering, Repudiation, Information disclosure, DoS, Elevation)
- Identify threats before writing code
- Create mitigations for each threat

**Banned Functions:**
- List of unsafe C/C++ functions (strcpy, sprintf, etc.)
- Compiler warnings for banned function use
- Safe alternatives provided

**Security Tools:**
- Static analysis in CI/CD
- Fuzz testing for input handling
- Binary analysis for vulnerabilities

---

## One Engineering System (1ES)

### What is 1ES?

Microsoft's unified engineering platform providing:
- Standardized build and release pipelines
- Common security and compliance tools
- Consistent developer experience
- Centralized telemetry and monitoring

### Quality Benefits

| Benefit | Description |
|---------|-------------|
| Consistency | Same quality tools across all products |
| Compliance | Built-in security and privacy checks |
| Efficiency | Shared infrastructure and tooling |
| Visibility | Centralized metrics and dashboards |

### Pipeline Quality Gates

Standard gates in 1ES pipelines:
1. Build succeeds
2. Unit tests pass
3. Static analysis clean
4. Security scan clean
5. Code coverage threshold met
6. Performance benchmarks pass

---

## Feature Flags and Safe Deployment

### Feature Flags (Experimentation)

Microsoft uses feature flags extensively:

```
if (featureFlags.isEnabled("new-search-algorithm", user)) {
    return newSearchAlgorithm(query);
} else {
    return oldSearchAlgorithm(query);
}
```

**Benefits:**
- Separate deployment from release
- Gradual rollout to users
- Quick disable without redeploy
- A/B testing built-in

### Safe Deployment Practices

**Ring-based deployment:**

| Ring | Audience | Purpose |
|------|----------|---------|
| Ring 0 | Dev team | Immediate feedback |
| Ring 1 | Internal users | Broader testing |
| Ring 2 | Early adopters | Real-world validation |
| Ring 3 | All users | Full release |

**Deployment health signals:**
- Error rates
- Performance metrics
- User engagement
- Crash rates

Automatic rollback if health degrades.

---

## Shift-Left Testing

### Philosophy

"Shift left" = move quality activities earlier in the development cycle.

```
Traditional:    Code → Build → Test → Fix → Release
                                ↑
                           Bugs found late (expensive)

Shift Left:     Test → Code → Test → Build → Test → Release
                  ↑      ↑            ↑
              Requirements  Unit    Integration
              validation    tests   tests
```

### Microsoft's Shift-Left Practices

| Practice | When | Purpose |
|----------|------|---------|
| Spec reviews | Before coding | Catch design issues |
| Unit tests | During coding | Verify logic |
| Static analysis | At commit | Find bugs automatically |
| Integration tests | At PR | Verify interactions |
| Security scans | In pipeline | Find vulnerabilities |

### Combined Engineering

Microsoft eliminated separate test teams:
- Developers own quality end-to-end
- No "throw over the wall" to QA
- Testing is everyone's responsibility
- Quality engineers focus on test infrastructure

---

## Telemetry-Driven Quality

### Customer-Reported vs Detected

Microsoft tracks quality through telemetry:

| Source | Example Metrics |
|--------|-----------------|
| Crashes | Crash rate, top crash buckets |
| Hangs | Hang rate, hang duration |
| Errors | Error codes, failure rates |
| Performance | Load time, response time |
| Usage | Feature adoption, user flows |

### Quality Metrics

**Key metrics tracked:**

```
Reliability = Successful sessions / Total sessions

Performance = Sessions meeting perf bar / Total sessions

Satisfaction = (Users not reporting issues) / Total users
```

### Data-Driven Decisions

Telemetry enables:
- Prioritize fixes by user impact
- Measure quality improvements
- Detect regressions quickly
- Understand real usage patterns

---

## Live Site Culture

### "Live Site First"

Modern Microsoft prioritizes production health:
- On-call rotations for all services
- Incident management processes
- Regular live site reviews
- Customer impact as top priority

### Incident Response

| Severity | Response Time | Example |
|----------|---------------|---------|
| Sev 0 | 15 minutes | Service down for all users |
| Sev 1 | 30 minutes | Major feature broken |
| Sev 2 | 4 hours | Feature degraded |
| Sev 3 | Next business day | Minor issue |

### Postmortem Process

After major incidents:
1. Document timeline
2. Identify root cause
3. Define repair items
4. Review with leadership
5. Track repair item completion

---

## Key Practices Summary

| Practice | Description |
|----------|-------------|
| SDL | Security built into development lifecycle |
| 1ES | Unified engineering platform |
| Feature flags | Separate deployment from release |
| Ring deployment | Gradual, safe rollouts |
| Shift-left | Early quality activities |
| Telemetry | Data-driven quality decisions |

---

## Evolution Over Time

| Era | Focus | Key Change |
|-----|-------|------------|
| 1990s | Ship features | "Shipping is a feature" |
| 2000s | Security | SDL, Trustworthy Computing |
| 2010s | Cloud | DevOps, continuous delivery |
| 2020s | AI/ML | Automated testing, intelligent monitoring |

---

## Related Topics

- [Security Testing](../../attributes/security/) — Security verification
- [SRE Practices](sre/) — Reliability engineering
- [CI/CD Quality](../project-quality/) — Pipeline quality gates

---

## Further Reading

- [Microsoft Security Development Lifecycle](https://www.microsoft.com/en-us/securityengineering/sdl) — Official SDL site
- [SDL Practices](https://www.microsoft.com/en-us/securityengineering/sdl/practices) — 10 security practices
- [SDL How-To Guide](https://www.microsoft.com/en-us/securityengineering/sdl/howto) — Implementation guidance
- "The DevOps Handbook" — Kim, Humble, Debois, Willis (IT Revolution, 2016)
- "Accelerate" — Forsgren, Humble, Kim (IT Revolution, 2018)

---

{: .highlight }
**Disclaimer:** AI is used for text polishing and explaining. Authors have verified all facts and claims. In case of an error, feel free to file an issue.
