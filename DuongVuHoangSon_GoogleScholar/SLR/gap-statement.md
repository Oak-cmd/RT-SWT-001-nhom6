# 1.6 Research Gap

## Phân tích Evidence Table

Sau khi xem xét 6 papers được đưa vào evidence table, nhóm trả lời 4 câu hỏi chính như sau:

### 1. LLM nào chưa được nghiên cứu sâu?
Hầu hết các nghiên cứu tập trung vào **GPT-3.5, GPT-4 / GPT-4o, Gemini, Claude 3**.  
**Chưa có** nghiên cứu nào đánh giá sâu hiệu suất của **GPT-4o zero-shot** trên quy mô dataset lớn và đa dạng trong việc sinh Gherkin scenarios.

### 2. "Semantic similarity" được đo như thế nào?
Các papers chủ yếu sử dụng **METEOR, BERTScore, ROUGE-L, LLM-as-a-judge**, hoặc human evaluation.  
**Chưa có** paper nào sử dụng **embedding-based semantic similarity** (ví dụ: Sentence-Transformer + Cosine Similarity) để so sánh Gherkin được sinh ra với expected behavior.

### 3. Executable syntax được kiểm tra như thế nào?
Một số papers kiểm tra syntax qua **Gherkin-lint** hoặc đo code coverage.  
**Chưa có** nghiên cứu nào kết hợp kiểm tra **executable syntax** (không lỗi cú pháp khi parse) cùng với **semantic similarity cao**.

### 4. Hạn chế nào của các nghiên cứu trước chưa được khắc phục?
- Dataset nhỏ, single company/context
- Thiếu metric semantic similarity mạnh (≥ 0.85)
- Chưa kết hợp cả hai tiêu chí: **semantic similarity cao** + **executable syntax**

---

## GAP Statement

**Tất cả 6 papers** được reviewed đều tập trung vào việc sử dụng LLM hoặc các phương pháp tự động để hỗ trợ sinh hoặc cải thiện Gherkin scenarios từ user stories/requirements.

Tuy nhiên, **KHÔNG CÓ paper nào**:
1. Sử dụng **GPT-4o** (hoặc các model mới) với **zero-shot prompting** trên dataset lớn và đa dạng;
2. Đo lường **semantic similarity** bằng embedding-based metrics (cosine similarity với Sentence-Transformer) so với expected behavior;
3. Kết hợp kiểm tra **executable syntax** (không lỗi cú pháp) cùng với ngưỡng **semantic similarity ≥ 0.85**.

**→ GAP**: Hiện tại chưa có nghiên cứu nào đánh giá toàn diện khả năng của LLM (đặc biệt là GPT-4o) trong việc tự động sinh Gherkin scenarios từ user stories viết theo format **Connextra**, đồng thời đảm bảo cả **semantic similarity cao (≥ 0.85)** với expected behavior và **executable syntax không lỗi**.

**→ Contribution của nghiên cứu này**: 
Nghiên cứu sẽ thực hiện đánh giá thực nghiệm GPT-4o (zero-shot và few-shot) trên bộ user stories thực tế, đo lường semantic similarity bằng Sentence-Transformer và kiểm tra executable rate bằng Gherkin parser, nhằm lấp khoảng trống trên.