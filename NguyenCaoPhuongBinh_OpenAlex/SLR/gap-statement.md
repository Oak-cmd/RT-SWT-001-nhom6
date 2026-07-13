# Gap Statement — LLM for Acceptance Test Automation (BDD/Gherkin)
Evidence table: N = 19 paper

## Các khoảng trống phát hiện

### GAP-T (Technology): Thiếu đánh giá chuyên sâu về GPT-4o trong cấu hình tất định (Temp=0)
Mặc dù GPT-4o đã được đề cập trong các nghiên cứu gần đây, hầu hết tập trung vào khả năng sinh mã thực thi hoặc đánh giá chung. Chưa có nghiên cứu nào tập trung kiểm chứng cấu hình **zero-shot với temperature=0** để đảm bảo tính tái lập (reproducibility) trong kỹ thuật phần mềm khi sinh kịch bản Gherkin.
**Bằng chứng:** [Cột Tool/LLM] 
- Paper **ID 11 (Nettur 2024)** sử dụng GPT-4o cho mã Cypress nhưng tập trung vào kỹ thuật few-shot chain.
- Paper **ID 3 (Rathnayake 2026)** so sánh GPT-4o với các LLM khác nhưng chưa nhấn mạnh vào tính tất định (Temp=0) làm tiêu chuẩn cốt lõi.

### GAP-M (Metric): Thiếu sự kết hợp giữa độ tương đồng ngữ nghĩa ngưỡng cao (>= 0.85) và tỷ lệ thực thi cú pháp (>= 80%)
Đa số các nghiên cứu sử dụng metrics NLP truyền thống (BLEU/ROUGE) hoặc đánh giá cảm tính của con người (Likert). Rất ít nghiên cứu sử dụng **Cosine Similarity (SBERT)** với một ngưỡng thành công định lượng khắt khe như **0.85** kết hợp đồng thời với **tỷ lệ thực thi cú pháp** tự động vượt ngưỡng **80%**.
**Bằng chứng:** [Cột Metric] 
- Paper **ID 11 (Farchi 2025)** sử dụng Cosine Similarity nhưng chỉ đạt mức trung bình 0.78.
- Paper **ID 8 (Karpurapu 2024)** và **ID 4 (Almeyda 2025)** đo độ chính xác cú pháp nhưng không kết hợp đo lường ngữ nghĩa chuyên sâu qua embedding.

### GAP-D (Dataset): Giới hạn về việc áp dụng User Story định dạng chuẩn Connextra
Nhiều nghiên cứu sử dụng các yêu cầu tự nhiên (NL) tự do hoặc các tập dữ liệu đặc thù (luật pháp, xe tự hành). Chưa có nghiên cứu nào thực hiện đánh giá GPT-4o trên một tập dữ liệu User Story định dạng chuẩn **Connextra** (As a... I want... So that...) để đo lường khả năng chuyển đổi sang kịch bản BDD có cấu trúc.
**Bằng chứng:** [Cột Dataset] 
- Paper **ID 21 (Hassani 2026)** và **ID 20 (Hassaniahari 2026)** sử dụng quy định an toàn thực phẩm (SFCR).
- Paper **ID 2 (Ferreira 2025)** chỉ sử dụng 13 JIRA issues với quy mô nhỏ.

## Phát biểu GAP tổng hợp
Hiện nay chưa có nghiên cứu nào đánh giá hiệu suất của mô hình **GPT-4o** (cấu hình **zero-shot, temperature=0**) trong việc sinh kịch bản BDD/Gherkin từ **User Story định dạng Connextra** dựa trên các chỉ số định lượng khắt khe: **độ tương đồng ngữ nghĩa Cosine Similarity >= 0.85** và **tỷ lệ kịch bản đúng cú pháp thực thi được >= 80%**.