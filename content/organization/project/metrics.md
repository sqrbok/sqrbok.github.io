---
title: Quality Metrics
parent: Project Quality
nav_order: 3
layout: default
---

# Project Quality Metrics

Quality metrics provide objective, quantitative measures of project quality, enabling data-driven decisions and tracking progress toward quality goals.

---

## What are Project Quality Metrics?

Project quality metrics measure specific aspects of product and process quality within the context of a project, helping to:

- Track progress toward quality goals
- Identify quality trends and patterns
- Make informed decisions about releases
- Communicate quality status to stakeholders
- Enable continuous improvement

---

## Key Topics

### Types of Project Metrics

**Product Metrics** - Characteristics of the software:

- Defect density (defects per KLOC or function point)
- Code complexity (cyclomatic complexity, nesting depth)
- Code coverage (line, branch, path coverage)
- Technical debt (estimated remediation effort)
- Performance metrics (response time, throughput)

**Process Metrics** - Effectiveness of quality processes:

- Defect detection effectiveness (% found in each phase)
- Review effectiveness (defects found per review hour)
- Test effectiveness (defects found by testing vs. production)
- Defect removal efficiency (defects removed / total defects)
- Test execution rate (tests per day)

**Project Metrics** - Overall project quality indicators:

- Defect discovery rate (defects found over time)
- Defect closure rate (defects fixed over time)
- Defect age (time from detection to closure)
- Test pass rate (% of tests passing)
- Escaped defects (found in production)

### Leading vs. Lagging Indicators

**Leading indicators** predict future quality:

- Code review coverage
- Unit test coverage
- Static analysis warnings
- Complexity trends
- Test automation percentage

**Lagging indicators** measure historical quality:

- Defect counts
- Customer complaints
- Production incidents
- Downtime
- Support costs

### Metric Selection

Choosing appropriate metrics using GQM:

1. **Goal** - What do you want to achieve?
2. **Question** - What do you need to know?
3. **Metric** - What will you measure?

**Example**:

- Goal: Improve release quality
- Question: Are we finding defects early?
- Metric: Defect detection efficiency (% found before production)

### Metric Thresholds

Establishing acceptable ranges:

- **Target** - Desired performance level
- **Threshold** - Minimum acceptable level
- **Stretch goal** - Aspirational excellence level

Example for code coverage:

- Target: 80%
- Threshold: 70% (minimum for release)
- Stretch: 90%

---

## Common Project Quality Metrics

### Defect Metrics

**Defect Density**:

```
Defect Density = Total Defects / Size (KLOC or FP)
```

**Defect Removal Efficiency (DRE)**:

```
DRE = Defects Found Before Release / Total Defects × 100%
```

**Defect Injection Rate**:

```
Injection Rate = Defects Found / Time Period
```

**Defect Closure Rate**:

```
Closure Rate = Defects Fixed / Time Period
```

### Test Metrics

**Code Coverage**:

```
Coverage = Lines Executed / Total Lines × 100%
```

**Test Effectiveness**:

```
Test Effectiveness = Defects Found by Testing / Total Defects
```

**Test Execution Rate**:

```
Execution Rate = Tests Run / Tests Planned × 100%
```

**Test Pass Rate**:

```
Pass Rate = Tests Passed / Tests Executed × 100%
```

### Review Metrics

**Review Coverage**:

```
Coverage = Lines Reviewed / Total Lines × 100%
```

**Review Efficiency**:

```
Efficiency = Defects Found / Review Hours
```

**Inspection Defect Density**:

```
Density = Defects Found / KLOC Reviewed
```

---

## Metric Collection and Tracking

### Data Collection

Sources of metric data:

- Issue tracking systems (Jira, GitHub Issues)
- Test management tools (TestRail, Zephyr)
- Code coverage tools (JaCoCo, Istanbul)
- Static analysis tools (SonarQube, ESLint)
- CI/CD systems (Jenkins, GitLab CI)
- Version control systems (Git analytics)

### Visualization

Effective metric displays:

- **Trend charts** - Show change over time
- **Control charts** - Monitor process stability
- **Burn-down charts** - Track defect resolution
- **Heat maps** - Identify problem areas
- **Dashboards** - Provide at-a-glance status

### Reporting Frequency

Appropriate cadence for different audiences:

- **Daily** - Team dashboards, build quality
- **Weekly** - Project manager, sprint metrics
- **Monthly** - Stakeholders, executive summary
- **Quarterly** - Strategic review, trend analysis

---

## Using Metrics for Decision Making

### Release Readiness

Quality gates based on metrics:

- Zero critical defects
- < 5 high-severity open defects
- > 85% code coverage
- > 95% test pass rate
- < 2.0 defects per KLOC
- All planned tests executed

### Risk Assessment

Using metrics to identify risks:

- Increasing defect injection rate → quality process issues
- Low code coverage in critical modules → inadequate testing
- High cyclomatic complexity → maintainability risk
- Defects concentrated in few modules → architectural issues

### Resource Allocation

Metrics-driven resource decisions:

- Focus testing on high-defect areas
- Allocate code review time to complex modules
- Prioritize refactoring of high-debt components
- Adjust team size based on defect trends

---

## Metric Pitfalls and Best Practices

### Pitfalls to Avoid

- Measuring too much (analysis paralysis)
- Gaming metrics (optimizing metric instead of quality)
- Ignoring context (comparing across different projects)
- Not acting on metrics (measurement without improvement)
- Setting metrics as targets (Goodhart's Law)

### Best Practices

1. **Start simple** - Begin with 3-5 core metrics
2. **Align with goals** - Ensure metrics support quality objectives
3. **Automate collection** - Reduce manual effort and errors
4. **Review regularly** - Analyze trends, don't just report numbers
5. **Act on insights** - Metrics should drive improvements
6. **Communicate clearly** - Make metrics understandable to all stakeholders
7. **Evolve metrics** - Adjust as project and needs change

---

## Metric Examples by Project Type

### Web Application

- API response time (p95, p99)
- JavaScript error rate
- Lighthouse performance score
- Accessibility compliance percentage
- Security vulnerability count

### Mobile Application

- Crash rate (crashes per user session)
- App store rating
- Load time on median device
- Battery consumption
- Network data usage

### Embedded System

- Memory usage (peak, average)
- CPU utilization
- Response time to interrupts
- Code size (ROM/RAM)
- Safety certification compliance

---

{: .note }
**Status**: Placeholder. Detailed content with calculation examples, tool guides, and dashboard templates will be added.

---

{: .highlight }
**Disclaimer:** AI is used for text polishing and explaining. Authors have verified all facts and claims. In case of an error, feel free to file an issue.
