# GAP Statement

**Topic:** LLM for Acceptance Test Automation (BDD/Gherkin)
**Systematic Literature Review · 2026**
123 records retrieved → 35 included

---

## Research Question (refined)

> "Does GPT-4o zero-shot (temperature = 0) generate Gherkin acceptance test scenarios that achieve cosine semantic similarity ≥ 0.85 with expert-written scenarios AND executable syntax rate ≥ 80% when applied to Connextra-format user stories from SE projects?"

---

## GAP Statement

**Tất cả 35 papers** được reviewed đều tập trung vào việc sử dụng LLM hoặc các phương pháp tự động để hỗ trợ sinh hoặc cải thiện Gherkin scenarios từ user stories/requirements.

Tuy nhiên, **KHÔNG CÓ paper nào**:

1. Sử dụng **GPT-4o** với **zero-shot prompting** (temperature = 0) trên dataset từ ≥ 3 dự án SE độc lập;
2. Đo lường **semantic similarity** bằng embedding-based metrics (cosine similarity với **all-MiniLM-L6-v2**) so với expert-written Gherkin baseline;
3. Kết hợp kiểm tra **executable syntax** (không lỗi cú pháp) cùng với ngưỡng **semantic similarity ≥ 0.85** trong cùng một thí nghiệm có kiểm soát.

**→ GAP:** Hiện tại chưa có nghiên cứu nào đánh giá toàn diện khả năng của LLM (đặc biệt là GPT-4o) trong việc tự động sinh Gherkin scenarios từ user stories viết theo format **Connextra**, đồng thời đảm bảo cả **semantic similarity cao (≥ 0.85)** với expected behavior và **executable syntax không lỗi (≥ 80%)**.

**→ Contribution của nghiên cứu này:**
Nghiên cứu sẽ thực hiện đánh giá thực nghiệm GPT-4o (zero-shot, temperature = 0) trên bộ user stories thực tế từ ≥ 3 dự án SE, đo lường semantic similarity bằng all-MiniLM-L6-v2 (Sentence-Transformer) và kiểm tra executable rate bằng Cucumber/Gherkin parser, nhằm lấp khoảng trống trên.


