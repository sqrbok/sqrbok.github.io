---
title: Agile Retrospectives
parent: Industry Practices
nav_order: 3
layout: default
---

# Agile Retrospectives

Agile Retrospectives are regular intervals where a software development team reflects on its performance to become more effective, tuning and adjusting its behavior accordingly {% cite lehtinen2017retrospectives %}. Grounded in the final principle of the Agile Manifesto, these meetings implement Software Process Improvement (SPI) principles of motivating all involved parties and creating a learning organization.

## Purpose and Core Mechanism

The primary purpose of a retrospective is to provide the team an "opportunity to inspect itself" {% cite lehtinen2017retrospectives %}. The core mechanism follows a structured five-phase model {% cite matthies2019retrospective %}:

1. **Set the Stage**: Create a safe environment for discussion
2. **Gather Data**: Collect observations about the iteration
3. **Generate Insights**: Identify patterns and root causes
4. **Decide What to Do**: Create actionable improvements
5. **Close**: Wrap up and appreciate contributions

### Key Elements

- **Target Identification**: Teams discuss the finished iteration, focusing on both successes and challenges
- **Reflection**: Practitioners use root cause analysis to investigate underlying causes of problems rather than just fixing immediate errors (double-loop learning)
- **Actionable Output**: The tangible result is a list of action items to be implemented in the following iteration

## Structured Retrospective Activities

To facilitate team interaction and overcome "retrospective smells" like the "Blame Game," various activities are used {% cite matthies2019retrospective %}:

### Sailboat

A metaphor-based activity where the team identifies:
- **Wind**: Positives/strengths pushing forward
- **Anchors**: Negatives/weaknesses holding back
- **Sun**: Opportunities on the horizon
- **Icebergs**: Threats/dangers ahead

### Five Whys

A root-cause analysis tool where teams repeatedly ask "Why?" (typically four to seven times) to find the deepest cause of a specific technical or process issue.

### Six Thinking Hats

Based on the work of Edward de Bono, this activity forces team members to look at iterations from six distinct metaphorical viewpoints (e.g., positive vs. negative framing) to mitigate Group Think {% cite matthies2019retrospective %}.

### Peaks and Valleys Timeline

Participants plot their emotional journey through the sprint on a mood graph to relate different views on shared events.

## Data-Driven Retrospectives

Matthies et al. (2020) argue that traditional retrospectives are limited because they depend solely on the subjective perceptions of team members {% cite matthies2020mining %}. To complement these views, teams can use Mining Software Repositories (MSR) to build a data-informed perspective.

### Repository Mining Approaches

| Activity | Purpose | Data Source |
|----------|---------|-------------|
| **Health Checks** | Collect measurements on best practices (code coverage, commit frequency) | Version control, CI/CD |
| **Remedy Appraisal** | Verify if previous actions were effective | Issue trackers, metrics |

### Artifact Sources

- **Version Control (git)**: Code diffs, commit frequency, unique contributors
- **Issue Trackers (Jira)**: Status updates, bug counts, story completion
- **Software Tests (Jenkins)**: Build status, test coverage, failure rates

## Common Problems and Countermeasures

Research by Matthies et al. (2019) mapped common "retrospective ailments" to specific activities that serve as countermeasures {% cite matthies2019retrospective %}:

| Problem | Countermeasure | How It Helps |
|---------|----------------|--------------|
| **No Preparation** | Sailboat, Futurespective | Provide inherent agenda for topic clustering |
| **Not Speaking Up** | Open the Box, Peaks and Valleys | Silent brainstorming gives thinking time |
| **All Talk–No Action** | Reverse Brainstorming | "How to make it worst?" then invert results |
| **Blame Game** | Guess Who | Answer from teammate's perspective to foster empathy |

## Empirical Findings: What Teams Actually Discuss

In a three-year longitudinal study of 37 retrospectives, Lehtinen et al. (2017) analyzed 879 statements to understand discussion trends {% cite lehtinen2017retrospectives %}:

### Key Findings

**Controllability Bias**: 75% of all statements were related to topics close to and controllable by the team, such as sprint planning and implementation.

**Frequency Statistics**:
- Implementation work discussed in **100%** of meetings
- Negative experiences: **51%** of statements
- Positive experiences: **29%** of statements

### Types of Recurring Discussions

| Type | Description | Example |
|------|-------------|---------|
| **Naturally Recurring** | Topics that naturally reappear | High bug counts |
| **Unsolvable** | Persistent challenges | Estimation accuracy |
| **Trivial Scapegoats** | Surface issues hiding deeper problems | Blaming poor specs to hide communication issues |

### Data Alignment Findings

The study revealed important biases {% cite matthies2020mining %}:
- "Low bug count" statements typically occurred when repository registered ≤90 open defects
- Comments on "poor estimation accuracy" often did not match actual repository data, suggesting participant bias

This underscores the value of combining subjective retrospective discussions with objective repository data for more accurate process improvement.

---

### References

{% bibliography --cited %}

---

{: .highlight }
**Disclaimer:** AI is used for text summarization, polishing and explaining. Authors have verified all facts and claims. In case of an error, feel free to file an issue.
