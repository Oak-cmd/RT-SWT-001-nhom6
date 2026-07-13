# Hypotheses

**Study:** GPT-4o Zero-Shot Gherkin Generation from Connextra User Stories  
**Derived from:** `01_rq.md` — Refined RQ (final)

> Each RQ maps to one H0/H1 pair. H0 is the null hypothesis (negation of what we aim to demonstrate). H1 is the research hypothesis (the expected result).

---

## RQ1 — Semantic Similarity

**Question:** Does GPT-4o zero-shot (temperature = 0) generate Gherkin scenarios with cosine semantic similarity ≥ 0.85 compared to expert-written scenarios?

| | Hypothesis |
|---|---|
| **H0₁** | The mean cosine semantic similarity (all-MiniLM-L6-v2) between GPT-4o zero-shot generated Gherkin scenarios and expert-written scenarios is **≤ 0.85** — i.e., GPT-4o does **not** reach the similarity threshold. |
| **H1₁** | The mean cosine semantic similarity (all-MiniLM-L6-v2) between GPT-4o zero-shot generated Gherkin scenarios and expert-written scenarios is **> 0.85** — i.e., GPT-4o **does** reach the similarity threshold. |

**Statistical test:** Wilcoxon signed-rank test (one-sample, non-parametric; similarity scores are bounded and unlikely to be normally distributed)  
**Significance level:** α = 0.05  
**Interpretation example:** If p = 0.03 < 0.05, we reject H0₁ and conclude that the mean similarity significantly exceeds 0.85.

---

## RQ2 — Executable Syntax Rate

**Question:** Does GPT-4o zero-shot (temperature = 0) generate Gherkin scenarios with a Cucumber-executable syntax rate ≥ 80%?

| | Hypothesis |
|---|---|
| **H0₂** | The proportion of GPT-4o zero-shot generated Gherkin scenarios that are Cucumber-executable is **≤ 0.80** — i.e., GPT-4o does **not** reach the executability threshold. |
| **H1₂** | The proportion of GPT-4o zero-shot generated Gherkin scenarios that are Cucumber-executable is **> 0.80** — i.e., GPT-4o **does** reach the executability threshold. |

**Statistical test:** Binomial test (one-tailed, p₀ = 0.80)  
**Significance level:** α = 0.05  
**Interpretation example:** If p = 0.03 < 0.05, we reject H0₂ and conclude that the executable syntax rate is significantly above 80%.

---

## Summary Table

| RQ | Metric | H0 | H1 | Test | α |
|----|--------|----|----|------|---|
| RQ1 | μ cosine similarity (all-MiniLM-L6-v2) | μ_similarity ≤ 0.85 | μ_similarity > 0.85 | Wilcoxon signed-rank | 0.05 |
| RQ2 | Executable syntax rate (Cucumber) | executable_rate ≤ 0.80 | executable_rate > 0.80 | Binomial test (one-tailed, p₀ = 0.80) | 0.05 |

---

## Grounding in SLR Evidence

| Hypothesis | Evidence basis |
|------------|---------------|
| H0₁ / H1₁ threshold = 0.85 | Alinezhadtilaki & Evans (2025) report mean BERT-cosine = 0.79; 0.85 is the stricter research-grade bar above all prior reported values |
| H0₂ / H1₂ threshold = 0.80 | Zero-shot baseline 76% (Karpurapu 2024); few-shot range 81–87% (Ferreira 2025; Fonseca 2025; Nettur 2025); 80% is the minimum practical usability floor for zero-shot output |
| Wilcoxon (not t-test) for RQ1 | Cosine similarity scores are bounded [0, 1] and skewed; normality assumption cannot be justified a priori |
| Binomial test for RQ2 | Executability is a binary outcome per scenario (pass/fail); binomial test is the exact method for proportion inference |

---

*Save to: `experiment/hypotheses.md`*
