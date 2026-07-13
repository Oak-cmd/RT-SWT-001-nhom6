# Hypotheses — LLM for Acceptance Test Automation (BDD/Gherkin)

**Topic:** Đối với user stories viết theo format Connextra, GPT-4o zero-shot tự động sinh
Gherkin scenarios + step definitions — có đạt semantic similarity ≥ 0.85 và executable
syntax không lỗi không?

---

## RQ1 — Semantic Similarity

|  | Phát biểu |
|--|---|
|H0| μ_similarity ≤ 0.85 — GPT-4o CHƯA ĐẠT ngưỡng similarity kỳ vọng |
|H1| μ_similarity > 0.85 — GPT-4o ĐẠT ngưỡng similarity kỳ vọng |

- Kiểm định: Wilcoxon signed-rank test (one-tailed)
- Mức ý nghĩa: α = 0.05
- Metric đo: Cosine similarity giữa Sentence-Transformer embedding của output LLM và expected behavior

### Giải thích kết quả:
| p-value | Kết luận |
|---|---|
| p = 0.03 | p < α (0.05) → Bác bỏ H0** → GPT-4o ĐẠT ngưỡng similarity ≥ 0.85  |
| p = 0.12 | p > α (0.05) → Không thể bác bỏ H0 → GPT-4o CHƯA đạt ngưỡng  |

---

## RQ2 — Executable Syntax

|  | Phát biểu |
|--|---|
|H0| executable_rate ≤ 0.80 — Tỷ lệ file Gherkin không lỗi cú pháp CHƯA đạt ngưỡng |
|H1| executable_rate > 0.80 — Tỷ lệ file Gherkin không lỗi cú pháp ĐẠT ngưỡng |

- Kiểm định: Binomial test (one-tailed, p₀ = 0.80)
- Mức ý nghĩa: α = 0.05
- Metric đo: Tỷ lệ file Gherkin parse thành công không lỗi cú pháp / tổng số file sinh ra

### Giải thích kết quả:
| p-value | Kết luận |
|---|---|
| p = 0.03 | p < α (0.05) → Bác bỏ H0 → Executable rate ĐẠT > 0.80  |
| p = 0.21 | p > α (0.05) → Không thể bác bỏ H0 → Executable rate CHƯA đạt  |

---

## Tóm tắt

| RQ | H0 (phủ định) | H1 (kỳ vọng) | Kiểm định |
|---|---|---|---|
| RQ1 | μ_similarity ≤ 0.85 | μ_similarity > 0.85 | Wilcoxon signed-rank, α=0.05 |
| RQ2 | executable_rate ≤ 0.80 | executable_rate > 0.80 | Binomial test, p₀=0.80, α=0.05 |
