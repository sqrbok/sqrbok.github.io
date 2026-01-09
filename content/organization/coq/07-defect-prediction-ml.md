---
title: Defect Prediction with ML
parent: Cost of Quality
nav_order: 7
layout: default
---

# ML-Based Defect Prediction

Machine Learning (ML)-based defect prediction leverages historical software metrics to identify potential source code anomalies early in the development lifecycle, aiming to save time and reduce the overall cost of software testing {% cite khleel2023bilstm %} {% cite bhutamapuram2022predictive %}. By moving beyond simple defect counting to predictive modeling, organizations can proactively allocate resources to high-risk modules.

## Bi-LSTM for Defect Prediction

Khleel & Nehéz (2023) proposed a Bidirectional Long Short-Term Memory (Bi-LSTM) neural network for software defect prediction {% cite khleel2023bilstm %}:

### Architecture

Unlike standard LSTMs that process data in one direction, Bi-LSTMs use two separate hidden layers to process input in both:
- **Forward direction** (past to future)
- **Backward direction** (future to past)

This allows the model to capture complex bidirectional temporal dependencies in code evolution.

### Experimental Results

Averages across six Java projects:

| Condition | Accuracy | F-Measure | AUC |
|-----------|----------|-----------|-----|
| Original (imbalanced) | 88% | **51%** | 76% |
| **+ Random Oversampling (ROS)** | **94%** | **94%** | **96%** |
| + SMOTE | 92% | 92% | 95% |

**Key improvement with ROS:** F-measure improved by **43 percentage points**.

## The Class Imbalance Problem

Software defect datasets are inherently imbalanced, typically containing many clean instances and very few defective ones {% cite gong2023overlap %}:

### Why Traditional Accuracy Misleads

| Metric | What It Measures | Problem with Imbalanced Data |
|--------|------------------|------------------------------|
| **Accuracy** | % of correct predictions | Reflects majority class dominance |
| **F-measure** | Harmonic mean of precision/recall | Reveals true minority class detection |

**Example from Bi-LSTM study:** The model achieved 88% accuracy on original data, yet F-measure was only **51%**. In extreme cases like the 'jedit' dataset, the model showed high accuracy while recording **0% precision and 0% recall**—failing to detect a single defect {% cite khleel2023bilstm %}.

### Why F-Measure Matters

F-measure reveals the model's true ability to identify the minority class (defects) rather than simply reflecting the majority class's dominance.

## Data Balancing Solutions

To mitigate bias toward non-defective code, oversampling techniques supplement the minority class {% cite khleel2023bilstm %}:

### Techniques Compared

| Technique | Method | How It Works |
|-----------|--------|--------------|
| **Random Oversampling (ROS)** | Replication | Randomly duplicates minority examples |
| **SMOTE** | Synthetic generation | Creates new samples from feature space |

### Impact on Performance (Bi-LSTM Study)

| Metric | Original | ROS | SMOTE | ROS Improvement |
|--------|----------|-----|-------|-----------------|
| Accuracy | 88% | **94%** | 92% | +6% |
| F-measure | 51% | **94%** | 92% | **+43%** |
| AUC | 76% | **96%** | 95% | +20% |

**Finding:** ROS consistently outperformed SMOTE in this study.

## Project-Specific Prediction Metrics

Bhutamapuram & Sadam (2022) argued that traditional ML metrics (accuracy, F-measure) fail to translate directly to project objectives like budget savings or risk mitigation {% cite bhutamapuram2022predictive %}:

### New Measures Proposed

| Measure | Full Name | What It Measures |
|---------|-----------|------------------|
| **RF** | Risk Factor | Risk from false negatives (missed severe defects) |
| **PSB** | Percent Saved Budget | % budget saved by correctly identifying clean modules |
| **RST** | Remaining Service Time | Hours needed to service remaining defective code |
| **GST** | Gratuitous Service Time | Wasted hours inspecting false positives |

### Traditional vs. Project Metrics

**Critical finding:** These metrics often contradict traditional ones.

| Metric | Traditional | Project-Specific |
|--------|-------------|------------------|
| Accuracy change | -0.96 pts | — |
| Budget savings (PSB) | — | **+0.33 pts** |
| Wasted time (GST) | — | **-10.73 hours** |

**Insight:** A model can be "less accurate" statistically while being **more valuable** to a project {% cite bhutamapuram2022predictive %}.

### Real-World Impact

Applied to four Java projects, the DST-DSP (Decision tree-based Self-Training) model achieved:

| Metric | Savings |
|--------|---------|
| Cost units saved | **4,302** |
| Service time reduced | **4,293 hours** |

## Economic Translation

Effective defect prediction enables "shifting left," catching defects in development where they are significantly cheaper to resolve {% cite knox1993modeling %}:

### Cost Assumptions

| Phase | Cost per Defect |
|-------|-----------------|
| Development | $100 |
| Post-release | $10,000 (100× multiplier) |

### Example: 1,000 Potential Defects

| Scenario | F-Measure | Caught Early | Escaped | Total Cost |
|----------|-----------|--------------|---------|------------|
| **Without balancing** | 51% | 510 | 490 | **$4.95M** |
| **With ROS balancing** | 94% | 940 | 60 | **$694K** |

### Net Business Value

| Metric | Value |
|--------|-------|
| Cost savings | **$4.26M** |
| Cost reduction | **86%** |
| Investment required | Data balancing + training |

## Practical Recommendations

### For Data Scientists

| Practice | Rationale |
|----------|-----------|
| **Always use F-measure or MCC** | Accuracy misleads with imbalanced data |
| **Apply oversampling (ROS or SMOTE)** | Addresses class imbalance |
| **Test on held-out imbalanced data** | Realistic evaluation |

### For Project Managers

| Practice | Rationale |
|----------|-----------|
| **Translate to project metrics** | PSB, RST, GST, RF map to business value |
| **Budget for prediction infrastructure** | ROI is 86%+ cost reduction |
| **Prioritize high-risk modules** | Focus testing resources effectively |

### For Quality Engineers

| Practice | Rationale |
|----------|-----------|
| **Integrate predictions into CI/CD** | Automated risk flagging |
| **Track historical metrics** | Improves model over time |
| **Combine with other quality gates** | Predictions are one signal among many |

## Summary

| Aspect | Traditional Approach | ML-Based Prediction |
|--------|---------------------|---------------------|
| Defect detection | Find after introduction | **Predict before testing** |
| Resource allocation | Uniform coverage | **Risk-based prioritization** |
| Cost structure | Reactive (failure costs) | **Proactive (prevention costs)** |
| ROI potential | — | **86% cost reduction** |

---

### References

{% bibliography --cited %}

---

{: .highlight }
**Disclaimer:** AI is used for text summarization, polishing and explaining. Authors have verified all facts and claims. In case of an error, feel free to file an issue.
