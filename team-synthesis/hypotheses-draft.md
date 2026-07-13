# Hypotheses Draft - LLM for Acceptance Test Automation
Ngày: 2026-06-10

## RQ1 - Semantic Similarity Preservation
H0: The median Cosine Similarity score of the GPT-4o generated scenarios is <=0.80.
H1: The median Cosine Similarity score of the GPT-4o generated scenarios is >0.80.
Statistical test dự kiến: Wilcoxon signed-rank test (a = 0.05$)

## RQ2 - Executable Syntax Validity
H0: The valid Executable Rate (error-free syntax) of GPT-4o generated scenarios is <=90%.
H1: The valid Executable Rate (error-free syntax) of GPT-4o generated scenarios is >90%.
Statistical test dự kiến: Binomial exact test (a = 0.05$)