# SQRBOK Development TODO

This document tracks missing sections and content to be developed based on the [overview diagram](images/overview.png).

## Status Legend
- ✅ **Complete** - Content exists and is comprehensive
- 🚧 **In Progress** - Partial content exists, needs expansion
- ❌ **Missing** - No content yet, needs to be created
- 📝 **Planned** - Placeholder exists, content needed

---

## 1. Defining Quality ✅

**Status**: Complete and recently restructured

### ✅ Quality Views
- [x] Transcendent view
- [x] Product-based view
- [x] User-based view
- [x] Manufacturing view
- [x] Value-based view

### ✅ Quality Models
- [x] Garvin's 8 dimensions
- [x] ISO/IEC 25010
- [x] Kano Model
- [x] McCall's Quality Model

### ✅ Metrics, Measuring & Adequacy of Quality Methods
- [x] Metric definitions
- [x] Types of metrics (product, process, resource)
- [x] Examples (LOC, complexity, defect density)
- [x] Development (GQM approach)
- [x] Pitfalls and anti-patterns

**Location**: `content/define/`
- `foundations/` - views, models, gurus
- `measurement/` - definitions, types, examples, development, pitfalls

---

## 2. Organisation / Quality Assurance 📝

**Status**: Placeholder only, needs comprehensive content

### ❌ Project Quality
**Priority**: High
**Content needed**:
- [ ] Quality planning in projects
- [ ] Quality goals and objectives
- [ ] Quality roles and responsibilities
- [ ] Project quality metrics and KPIs
- [ ] Quality gates and milestones

### ❌ Quality Processes
**Priority**: High
**Content needed**:
- [ ] Quality management processes
- [ ] Process improvement frameworks (PDCA, DMAIC)
- [ ] Process maturity models
- [ ] Quality audits and assessments
- [ ] Continuous improvement

### ❌ Cost of Quality
**Priority**: Medium
**Content needed**:
- [ ] Prevention costs
- [ ] Appraisal costs
- [ ] Internal failure costs
- [ ] External failure costs
- [ ] Cost-benefit analysis of quality activities
- [ ] ROI of quality investments

### ❌ Organizational Quality / CMMI
**Priority**: Medium
**Content needed**:
- [ ] CMMI overview and levels
- [ ] Process areas and practices
- [ ] Organizational maturity assessment
- [ ] ISO 9001 and quality standards
- [ ] Six Sigma in software
- [ ] Total Quality Management (TQM)

**Location**: `content/organization/`
**Suggested structure**:
```
organization/
├── index.md (update with comprehensive content)
├── project/
│   ├── index.md
│   ├── planning.md
│   ├── goals.md
│   └── metrics.md
├── processes/
│   ├── index.md
│   ├── improvement.md
│   ├── maturity.md
│   └── audits.md
├── cost/
│   ├── index.md
│   ├── categories.md
│   └── analysis.md
└── standards/
    ├── index.md
    ├── cmmi.md
    ├── iso9001.md
    └── six-sigma.md
```

---

## 3. Verification Methods: Basics + Advanced 🚧

**Status**: Partially complete, some gaps

### ✅ Overview: Definitions, Method Categories, Limitations, When to Use
- [x] V&V definitions
- [x] Static vs. dynamic methods
- [x] Manual vs. automated
- [x] Black box vs. white box
- [x] When to use each approach

**Location**: `content/verif/overview/`

### 🚧 Functional Testing (aka Black Box)
**Status**: Basic coverage exists, needs expansion

**Exists**:
- [x] Overview in testing/index.md
- [x] Black box vs. white box comparison

**Missing**:
- [ ] Equivalence partitioning (detailed guide)
- [ ] Boundary value analysis (with examples)
- [ ] Decision tables (construction and usage)
- [ ] State transition testing
- [ ] Use case testing
- [ ] Classification trees (detailed)

**Priority**: High
**Location**: `content/verif/overview/testing/` needs expansion

### 🚧 Structural Testing (aka White Box)
**Status**: Coverage metrics exist, specific techniques need detail

**Exists**:
- [x] Statement coverage
- [x] Branch coverage
- [x] Path coverage
- [x] Modified Condition/Decision Coverage (MC/DC)
- [x] Data flow testing overview

**Missing**:
- [ ] Detailed DefUse analysis with examples
- [ ] Control flow graphs
- [ ] Data flow graphs
- [ ] Loop testing strategies
- [ ] Integration with coverage tools

**Priority**: Medium
**Location**: `content/verif/coverage/` - some exists, needs practical examples

### ❌ Random Testing
**Priority**: Low
**Content needed**:
- [ ] Random input generation
- [ ] Monkey testing
- [ ] Fuzz testing basics
- [ ] When random testing is effective
- [ ] Limitations and challenges

**Location**: Create `content/verif/overview/testing/random.md`

### ❌ Metamorphic Testing
**Priority**: Low
**Content needed**:
- [ ] Metamorphic relations
- [ ] Test oracle problem
- [ ] Applications and examples
- [ ] When to use metamorphic testing

**Location**: Create `content/verif/overview/testing/metamorphic.md`

### ❌ Model-Based Testing
**Priority**: Medium
**Content needed**:
- [ ] Test generation from models
- [ ] State machine testing
- [ ] UML-based testing
- [ ] Model coverage criteria
- [ ] Tools (SpecExplorer, GraphWalker, etc.)

**Location**: Create `content/verif/overview/testing/model_based.md`

### ❌ Exploratory Testing
**Priority**: Medium
**Content needed**:
- [ ] Session-based testing
- [ ] Exploratory testing techniques
- [ ] Charters and note-taking
- [ ] When to use exploratory testing
- [ ] Combining with scripted testing

**Location**: Create `content/verif/overview/testing/exploratory.md`

### ✅ Static Analysis Overview
**Status**: Good coverage exists
- [x] Code reviews / inspections
- [x] Static analysis tools (linters, type checkers)
- [x] Model checking overview
- [x] Symbolic execution overview
- [x] Formal methods overview

**Location**: `content/verif/overview/analysis/`

**Improvements needed**:
- [ ] More practical examples for each technique
- [ ] Tool comparison matrices
- [ ] Integration guides for CI/CD

---

## 4. Specific Methods for Quality Properties ❌

**Status**: Placeholder only, entirely missing

**Priority**: Medium-High

This section should cover specialized techniques for specific quality attributes.

### ❌ Maintainability
**Content needed**:
- [ ] Technical debt measurement
- [ ] Design structure matrix
- [ ] Dependency analysis
- [ ] Refactoring strategies
- [ ] Code smell detection
- [ ] Maintainability index

**Suggested location**: `content/attributes/maintainability/`

### ❌ Reliability
**Content needed**:
- [ ] Reliability definitions and metrics
- [ ] Fault injection testing
- [ ] Reliability growth models
- [ ] MTBF, MTTR calculations
- [ ] Availability analysis
- [ ] Failure mode analysis

**Suggested location**: `content/attributes/reliability/`

### ❌ Performance
**Content needed**:
- [ ] Performance testing types (load, stress, spike, endurance)
- [ ] Performance metrics (response time, throughput, resource utilization)
- [ ] Profiling and benchmarking
- [ ] Queuing theory basics
- [ ] Performance modeling
- [ ] Tools (JMeter, Gatling, K6, etc.)

**Suggested location**: `content/attributes/performance/`

### ❌ Security
**Content needed**:
- [ ] Threat modeling (STRIDE, DREAD)
- [ ] Security testing techniques
- [ ] Penetration testing basics
- [ ] OWASP Top 10
- [ ] Secure coding principles
- [ ] Security code review
- [ ] Vulnerability scanning

**Suggested location**: `content/attributes/security/`

### ❌ Usability
**Content needed**:
- [ ] Usability heuristics
- [ ] User testing methods
- [ ] Accessibility testing (WCAG)
- [ ] Cognitive walkthrough
- [ ] A/B testing
- [ ] Usability metrics

**Suggested location**: `content/attributes/usability/`

**Suggested structure for attributes**:
```
attributes/
├── index.md (update with comprehensive overview)
├── maintainability/
│   ├── index.md
│   ├── technical_debt.md
│   ├── metrics.md
│   └── refactoring.md
├── reliability/
│   ├── index.md
│   ├── definitions.md
│   ├── testing.md
│   └── metrics.md
├── performance/
│   ├── index.md
│   ├── testing_types.md
│   ├── metrics.md
│   └── tools.md
├── security/
│   ├── index.md
│   ├── threat_modeling.md
│   ├── testing.md
│   └── owasp.md
└── usability/
    ├── index.md
    ├── heuristics.md
    ├── testing.md
    └── accessibility.md
```

---

## 5. Additional Content Gaps

### ❌ Advanced Verification Methods

**Priority**: Low-Medium

Not shown in overview but valuable additions:

- [ ] **Property-based testing** (QuickCheck, Hypothesis)
- [ ] **Mutation testing** (exists in coverage, but needs practical guide)
- [ ] **Concurrency testing** (race conditions, deadlocks)
- [ ] **Regression testing** strategies
- [ ] **Test data generation**
- [ ] **Combinatorial testing** (pairwise, n-way) - exists but needs examples

**Location**: Could go in `content/verif/advanced/`

### ❌ Testing in Modern Contexts

**Priority**: Medium

- [ ] **Microservices testing** (contract testing, service virtualization)
- [ ] **API testing** strategies
- [ ] **Mobile testing** (device fragmentation, platform differences)
- [ ] **Cloud testing** considerations
- [ ] **DevOps and continuous testing**
- [ ] **Shift-left testing**

**Location**: Could go in `content/verif/modern/`

### 📝 Material / Resources

**Status**: Placeholder exists

**Priority**: Low

**Content needed**:
- [ ] Recommended books by topic
- [ ] Key research papers (with summaries)
- [ ] Online courses and tutorials
- [ ] Tool catalogs by category
- [ ] Industry standards and certifications
- [ ] Communities and conferences

**Location**: `content/material/`

---

## 6. Cross-Cutting Improvements

### Documentation Quality

- [ ] Ensure all pages have AI disclaimer ✅ (Done)
- [ ] Add cross-references between related topics
- [ ] Create glossary of terms
- [ ] Add "Further Reading" sections consistently
- [ ] Include practical examples in all conceptual pages

### Navigation and Structure

- [x] Fix Jekyll navigation hierarchy ✅ (Done)
- [x] Restructure define section ✅ (Done)
- [ ] Add breadcrumb navigation
- [ ] Create topic-based learning paths
- [ ] Add search functionality improvements

### Visual Aids

- [ ] Create diagrams for key concepts
- [ ] Add flowcharts for decision-making
- [ ] Include code examples with syntax highlighting
- [ ] Add comparison tables
- [ ] Create process diagrams

### Interactive Elements

- [ ] Add self-assessment quizzes
- [ ] Include interactive calculators (e.g., cyclomatic complexity)
- [ ] Create decision trees for technique selection
- [ ] Add tool recommendation wizards

---

## 7. Priority Ranking

### Immediate (Next Sprint)
1. **Organization section** - Fill in project quality and processes
2. **Attributes/Performance** - Critical for most projects
3. **Functional testing techniques** - Expand with detailed examples
4. **Security basics** - Growing importance

### Short Term (1-2 months)
5. **Attributes/Reliability** - Complete the section
6. **Attributes/Maintainability** - Technical debt focus
7. **Model-based testing** - Increasingly relevant
8. **Exploratory testing** - Practical guidance

### Medium Term (3-6 months)
9. **Attributes/Usability** - Complete the picture
10. **Advanced verification methods**
11. **Cost of quality** - Economic justification
12. **CMMI and standards**

### Long Term (6+ months)
13. **Modern testing contexts** (microservices, cloud, etc.)
14. **Material/Resources** section
15. **Random and metamorphic testing**
16. **Interactive elements and tools**

---

## 8. Maintenance Tasks

### Regular Updates
- [ ] Keep tool lists current (quarterly review)
- [ ] Update standards references (annual review)
- [ ] Refresh examples with modern frameworks
- [ ] Review and update metrics thresholds
- [ ] Check for broken links (monthly)

### Community Contributions
- [ ] Set up contribution guidelines ✅ (Done)
- [ ] Create issue templates for content requests
- [ ] Establish review process for submissions
- [ ] Maintain contributor recognition

---

## Notes

- See `images/overview.png` for the handbook structure diagram
- All new content should include the AI disclaimer
- Follow the existing style and formatting conventions
- Use Jekyll front matter consistently (title, parent, nav_order, layout, has_children)
- Cross-reference related topics with markdown links
- Include practical examples and real-world applications

**Last Updated**: 2025-12-28
