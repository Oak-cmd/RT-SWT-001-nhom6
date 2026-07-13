# Hypotheses

## Purpose

Based on the refined research question and the identified research gaps, this study evaluates whether GPT-4o can generate Gherkin acceptance test scenarios that are both semantically faithful to the original user stories and syntactically executable.

Two research questions are investigated. Each research question is associated with a null hypothesis (H0) and an alternative hypothesis (H1).

---

## RQ1 — Semantic Similarity

### Research Question

Can GPT-4o zero-shot generate Gherkin acceptance test scenarios whose semantic meaning is sufficiently similar to expert-written scenarios?

### Metric

Cosine similarity computed using the all-MiniLM-L6-v2 sentence embedding model.

### Threshold

0.85

### Null Hypothesis (H0_1)

The semantic similarity between GPT-4o-generated Gherkin scenarios and expert-written Gherkin scenarios is less than or equal to 0.85.

H0_1: similarity <= 0.85

### Alternative Hypothesis (H1_1)

The semantic similarity between GPT-4o-generated Gherkin scenarios and expert-written Gherkin scenarios is greater than 0.85.

H1_1: similarity > 0.85

### Statistical Test

Wilcoxon Signed-Rank Test

### Significance Level

alpha = 0.05

---

## RQ2 — Executable Syntax

### Research Question

Can GPT-4o zero-shot generate Gherkin acceptance test scenarios that achieve an executable syntax rate of at least 80%?

### Metric

Executable syntax rate measured using automated Gherkin parsing.

### Threshold

80%

### Null Hypothesis (H0_2)

The executable syntax rate of GPT-4o-generated Gherkin scenarios is less than or equal to 80%.

H0_2: executable_rate <= 0.80

### Alternative Hypothesis (H1_2)

The executable syntax rate of GPT-4o-generated Gherkin scenarios is greater than 80%.

H1_2: executable_rate > 0.80

### Statistical Test

One-tailed Binomial Test

### Significance Level

alpha = 0.05

---

## Decision Rule

For both research questions:

- Reject H0 if p-value < 0.05.
- Fail to reject H0 if p-value >= 0.05.

---

## Expected Outcome

This study expects GPT-4o to:

1. Achieve semantic similarity greater than 0.85 when compared with expert-written Gherkin scenarios.

2. Achieve an executable syntax rate greater than 80% when validated using an automated Gherkin parser.

If both hypotheses are supported, the results will provide evidence that GPT-4o can effectively assist automated Behavior-Driven Development (BDD) scenario generation while maintaining both semantic quality and structural correctness.